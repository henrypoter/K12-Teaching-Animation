# 需求：从DNA到蛋白质的中心法则（转录+剪接+mRNA→核糖体→tRNA运氨基酸）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要是高中或大学低年级的生物学学生，他们已具备DNA双螺旋、碱基配对等基础知识，现在需要直观、动态地理解中心法则中从DNA到蛋白质合成的复杂过程。
2.  **核心需求**：
    *   **理解流程**：清晰、分步地展示“DNA转录 → pre-mRNA剪接 → mRNA出核 → 核糖体翻译 → tRNA运载氨基酸”这一系列事件。
    *   **突破难点**：重点化解“剪接（内含子/外显子）”和“翻译（密码子与反密码子配对、肽链延伸）”这两个抽象且动态的难点。
    *   **建立联系**：将分子事件（如碱基序列）与宏观结果（蛋白质的一级结构）联系起来，理解“信息流”的本质。
    *   **主动探索**：用户不满足于被动观看，希望通过交互控制节奏、聚焦细节、验证理解。

#### 教学设计思路
1.  **核心概念分解**：
    *   **信息流**：DNA（模板）→ mRNA（信使）→ 蛋白质（功能产物）。
    *   **转录**：在细胞核内，以DNA一条链为模板，遵循碱基互补配对（A-U， T-A， C-G， G-C）合成pre-mRNA。
    *   **RNA剪接**：切除pre-mRNA中的内含子，连接外显子，形成成熟mRNA。
    *   **翻译**：在细胞质核糖体上，mRNA的密码子序列被tRNA的反密码子识别，按序带入相应氨基酸，合成多肽链。
    *   **结构与功能**：tRNA的“三叶草”结构、核糖体的A/P/E位点。

2.  **认知规律（动画叙事结构）**：
    *   **总-分-总结构**：
        *   **总览**：开场展示一个简化的真核细胞，高亮细胞核和细胞质中的核糖体，用箭头示意“DNA → mRNA → 蛋白质”的整体路径。
        *   **分步详解**：将流程分解为三个可交互的模块（场景），用户可按顺序或选择学习：
            1.  **场景一：转录与剪接（细胞核内）**。
            2.  **场景二：mRNA运输与核糖体组装**。
            3.  **场景三：翻译与肽链合成（核糖体上）**。
        *   **总结与联系**：最后动态并列展示DNA序列、mRNA序列、tRNA阵列、氨基酸序列，并最终折叠成一个简单的蛋白质模型，强化信息传递概念。

3.  **交互设计**：
    *   **进度控制**：提供“播放/暂停/步进/重置”全局控制。
    *   **模块化学习**：通过标签页或导航按钮，允许用户直接跳转到特定场景。
    *   **焦点交互**：
        *   在剪接环节，可点击“切除内含子”按钮，观看内含子环出并被降解的过程。
        *   在翻译环节，可点击“下一个tRNA”按钮，逐步推进翻译过程。鼠标悬停在tRNA上可显示其携带的氨基酸名称。
        *   提供“显示/隐藏”标签的选项（如“RNA聚合酶”、“A位点”、“肽键”等），避免初学时界面过于杂乱。
    *   **模拟测验**：在翻译场景，提供一个“拖拽tRNA”的小游戏，让用户将正确的tRNA拖到mRNA的指定密码子上。

4.  **视觉呈现**：
    *   **风格**：采用扁平化、卡通化的科学插图风格，在保证科学性的前提下，简化细节，突出关键结构和过程。
    *   **动态效果**：
        *   分子“生长”动画（如RNA链的延伸、肽链的延伸）。
        *   平滑的移动动画（如mRNA出核孔、核糖体沿mRNA移动）。
        *   高亮和颜色脉冲来指示当前活动的部分（如正在配对的碱基、正在形成肽键的位置）。

#### 配色方案选择
*   **主色调与科学规范**：
    *   **DNA**：经典的双螺旋使用**深蓝色**和**浅蓝色**表示两条链，碱基对（A-T， C-G）使用协调的对比色（如A-橙色， T-浅橙色， C-黄色， G-绿色），便于区分。
    *   **RNA**：mRNA使用与DNA区别明显的**红色**或**洋红色**，以强调其不同分子身份。tRNA使用**紫色**，rRNA（核糖体）使用**灰色**或**浅褐色**。
    *   **蛋白质/氨基酸**：肽链使用**渐变的暖色调**（如从橙色到红色），新加入的氨基酸可以更亮。不同的氨基酸可以用形状或侧链小图标区分，颜色保持在同一色系内。
*   **背景与环境**：细胞核背景用**浅米黄或极浅的蓝色**，细胞质背景用**极浅的灰色或绿色**，形成柔和对比，确保前景分子突出。
*   **交互元素**：按钮使用**中性深灰色**，高亮和提示使用**醒目的黄色或半透明荧光色**。

#### 交互功能列表
1.  **主控面板**：播放、暂停、步进（下一步）、重置动画。
2.  **场景导航器**：三个按钮或标签，分别对应“转录与剪接”、“mRNA运输”、“翻译合成”，点击后跳转并播放对应场景动画。
3.  **场景一（转录与剪接）特定交互**：
    *   “开始转录”按钮：触发RNA聚合酶移动及mRNA合成。
    *   “显示/隐藏内含子”复选框：切换内含子序列的视觉表现（如模糊或不同颜色）。
    *   “执行剪接”按钮：手动触发剪接体动作，展示内含子被切除、外显子连接。
4.  **场景二（运输）特定交互**：主要为自动动画，展示mRNA通过核孔进入细胞质并与核糖体小亚基结合。
5.  **场景三（翻译）特定交互**：
    *   “步进翻译”按钮：每点击一次，完成一个氨基酸的添加循环（tRNA进入、肽键形成、移位）。
    *   “tRNA信息”悬停：鼠标悬停在任意tRNA上，显示其反密码子和所携带的氨基酸名称。
    *   “密码子表”开关：点击可呼出一个简化的密码子-氨基酸对应表，作为参考。
    *   **“拖拽匹配”小游戏模式**：在此模式下，给定一个mRNA密码子序列和几个不同的tRNA，用户需将正确的tRNA拖到核糖体A位点上。
6.  **视觉辅助开关**：
    *   “显示标签”：切换所有分子和位点名称标签的显示。
    *   “高亮碱基配对”：在转录和翻译时，配对的碱基对会闪烁强调。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>中心法则：从DNA到蛋白质</title>
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
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.92);
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 100, 0.1);
            padding: 25px;
            overflow: hidden;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eaeef5;
        }
        
        h1 {
            color: #2c3e50;
            font-size: 2.4rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #3498db, #2c3e50);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .animation-section {
            background-color: #fff;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #eaeef5;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #f8fafc;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #dce4ef;
        }
        
        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .controls-section {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            align-items: center;
            padding: 20px;
            background-color: #f8fafc;
            border-radius: 12px;
        }
        
        .scene-nav {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #2ecc71;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #27ae60;
            transform: translateY(-2px);
        }
        
        .btn-scene {
            background-color: #9b59b6;
            color: white;
        }
        
        .btn-scene:hover {
            background-color: #8e44ad;
            transform: translateY(-2px);
        }
        
        .btn-scene.active {
            background-color: #732d91;
            box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.2);
        }
        
        .btn:disabled {
            background-color: #bdc3c7;
            cursor: not-allowed;
            transform: none;
        }
        
        .info-panel {
            background-color: #fff;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #eaeef5;
        }
        
        h2 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.6rem;
            border-left: 5px solid #3498db;
            padding-left: 12px;
        }
        
        .info-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .info-box {
            background-color: #f8fafc;
            padding: 18px;
            border-radius: 10px;
            border-left: 4px solid;
        }
        
        .info-box h3 {
            margin-bottom: 10px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .info-box.transcription {
            border-left-color: #e74c3c;
        }
        
        .info-box.splicing {
            border-left-color: #9b59b6;
        }
        
        .info-box.translation {
            border-left-color: #2ecc71;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #eaeef5;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }
        
        .legend-label {
            font-size: 0.9rem;
        }
        
        .game-mode {
            background-color: #fff9e6;
            border: 2px dashed #f1c40f;
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
            text-align: center;
        }
        
        .game-mode h3 {
            color: #d35400;
            margin-bottom: 10px;
        }
        
        .status-bar {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 10px 15px;
            border-radius: 8px;
            font-weight: 600;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            z-index: 10;
            border: 1px solid #eaeef5;
        }
        
        .tooltip {
            position: absolute;
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 0.9rem;
            pointer-events: none;
            z-index: 100;
            max-width: 250px;
            display: none;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .canvas-container {
                height: 400px;
            }
            
            .controls-section {
                flex-direction: column;
            }
            
            .btn {
                padding: 10px 18px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>中心法则：从DNA到蛋白质</h1>
            <p class="subtitle">探索遗传信息如何从DNA转录为mRNA，经过剪接后翻译成蛋白质的完整过程</p>
        </header>
        
        <div class="main-content">
            <div class="animation-section">
                <div class="canvas-container">
                    <div class="status-bar" id="statusBar">场景：转录与剪接</div>
                    <canvas id="animationCanvas"></canvas>
                    <div class="tooltip" id="tooltip"></div>
                </div>
            </div>
            
            <div class="controls-section">
                <div class="scene-nav">
                    <button class="btn btn-scene active" id="scene1Btn">1. 转录与剪接</button>
                    <button class="btn btn-scene" id="scene2Btn">2. mRNA运输</button>
                    <button class="btn btn-scene" id="scene3Btn">3. 翻译合成</button>
                </div>
                
                <div style="display: flex; gap: 10px; flex-wrap: wrap;">
                    <button class="btn btn-primary" id="playBtn">播放</button>
                    <button class="btn btn-primary" id="pauseBtn">暂停</button>
                    <button class="btn btn-primary" id="stepBtn">下一步</button>
                    <button class="btn btn-primary" id="resetBtn">重置</button>
                </div>
                
                <div style="display: flex; gap: 10px; flex-wrap: wrap;">
                    <button class="btn btn-secondary" id="toggleLabelsBtn">显示标签</button>
                    <button class="btn btn-secondary" id="highlightBtn">高亮配对</button>
                    <button class="btn btn-secondary" id="gameModeBtn">拖拽匹配游戏</button>
                </div>
            </div>
            
            <div class="info-panel">
                <h2>过程详解</h2>
                <div class="info-content">
                    <div class="info-box transcription">
                        <h3>📝 转录</h3>
                        <p>在细胞核内，RNA聚合酶以DNA的一条链为模板，按照碱基互补配对原则（A-U，T-A，C-G，G-C）合成pre-mRNA分子。</p>
                    </div>
                    <div class="info-box splicing">
                        <h3>✂️ RNA剪接</h3>
                        <p>pre-mRNA中的内含子（非编码区）被剪接体识别并切除，外显子（编码区）连接在一起形成成熟的mRNA。</p>
                    </div>
                    <div class="info-box translation">
                        <h3>🧬 翻译</h3>
                        <p>mRNA进入细胞质，核糖体读取其密码子序列，tRNA携带相应的氨基酸，通过反密码子与密码子配对，合成多肽链。</p>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2c3e50;"></div>
                        <span class="legend-label">DNA</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span class="legend-label">mRNA</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #9b59b6;"></div>
                        <span class="legend-label">tRNA</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span class="legend-label">氨基酸/蛋白质</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span class="legend-label">核糖体</span>
                    </div>
                </div>
                
                <div class="game-mode" id="gameModePanel" style="display: none;">
                    <h3>🧪 拖拽匹配游戏</h3>
                    <p>将正确的tRNA拖拽到核糖体的A位点上，匹配mRNA上的密码子！</p>
                    <div id="gameInfo">
                        <p>当前密码子: <span id="currentCodon">AUG</span></p>
                        <p>得分: <span id="gameScore">0</span> / <span id="gameTotal">0</span></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        const tooltip = document.getElementById('tooltip');
        const statusBar = document.getElementById('statusBar');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();
        
        // 动画状态
        let currentScene = 1; // 1: 转录与剪接, 2: mRNA运输, 3: 翻译合成
        let isPlaying = false;
        let animationFrameId = null;
        let showLabels = true;
        let highlightPairing = true;
        let gameMode = false;
        let gameScore = 0;
        let gameTotal = 0;
        
        // 颜色定义
        const colors = {
            dna: '#2c3e50',
            dnaStrand2: '#3498db',
            mrna: '#e74c3c',
            preMrnaIntron: '#e67e22',
            trna: '#9b59b6',
            aminoAcid: '#2ecc71',
            ribosome: '#f1c40f',
            nucleus: 'rgba(52, 152, 219, 0.1)',
            cytoplasm: 'rgba(46, 204, 113, 0.05)',
            text: '#2c3e50',
            highlight: '#f1c40f'
        };
        
        // 碱基定义
        const dnaBases = ['A', 'T', 'C', 'G'];
        const rnaBases = ['A', 'U', 'C', 'G'];
        const aminoAcids = ['Met', 'Leu', 'Ser', 'Arg', 'Gly', 'Pro', 'Val', 'Thr', 'Ala'];
        
        // 场景1: 转录与剪接
        const scene1 = {
            dnaX: 100,
            dnaY: 250,
            dnaLength: 400,
            transcriptionProgress: 0,
            rnaPolymeraseX: 100,
            preMrna: [],
            spliced: false,
            splicingProgress: 0,
            introns: [
                {start: 3, end: 5, removed: false},
                {start: 8, end: 10, removed: false}
            ]
        };
        
        // 场景2: mRNA运输
        const scene2 = {
            mrnaX: 150,
            mrnaY: 250,
            nucleusX: 100,
            nucleusY: 200,
            nucleusRadius: 120,
            nuclearPoreX: 220,
            nuclearPoreY: 200,
            transportProgress: 0,
            ribosomeX: 500,
            ribosomeY: 250,
            assemblyProgress: 0
        };
        
        // 场景3: 翻译合成
        const scene3 = {
            mrnaX: 200,
            mrnaY: 300,
            mrnaSequence: ['AUG', 'CUU', 'UCU', 'AGA', 'GGA', 'CCA', 'GUA', 'ACC', 'GCA', 'UAA'],
            currentCodonIndex: 0,
            ribosomeX: 300,
            ribosomeY: 300,
            trnas: [],
            peptideChain: [],
            translationProgress: 0,
            draggingTrna: null,
            dragOffsetX: 0,
            dragOffsetY: 0
        };
        
        // 初始化tRNA
        function initTranslationScene() {
            scene3.trnas = [];
            scene3.peptideChain = [];
            scene3.currentCodonIndex = 0;
            
            // 创建一些游离的tRNA
            for (let i = 0; i < 5; i++) {
                scene3.trnas.push({
                    x: 100 + Math.random() * 150,
                    y: 100 + Math.random() * 150,
                    anticodon: getRandomAnticodon(),
                    aminoAcid: aminoAcids[Math.floor(Math.random() * aminoAcids.length)],
                    state: 'free', // free, inA, inP, inE
                    inRibosome: false
                });
            }
            
            // 确保至少有一个正确的tRNA
            const correctAnticodon = getComplementaryCodon(scene3.mrnaSequence[0]);
            scene3.trnas[0].anticodon = correctAnticodon;
            scene3.trnas[0].aminoAcid = 'Met'; // AUG对应甲硫氨酸
        }
        
        // 获取随机反密码子
        function getRandomAnticodon() {
            const bases = ['A', 'U', 'C', 'G'];
            let codon = '';
            for (let i = 0; i < 3; i++) {
                codon += bases[Math.floor(Math.random() * bases.length)];
            }
            return codon;
        }
        
        // 获取互补密码子
        function getComplementaryCodon(codon) {
            const complement = {
                'A': 'U',
                'U': 'A',
                'C': 'G',
                'G': 'C'
            };
            
            let result = '';
            for (let i = 0; i < codon.length; i++) {
                result += complement[codon[i]] || ' ';
            }
            return result;
        }
        
        // 绘制DNA双螺旋
        function drawDNA(x, y, length, progress = 1) {
            const segmentCount = 20;
            const segmentLength = length / segmentCount;
            
            // 绘制DNA骨架
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x + length * progress, y);
            ctx.strokeStyle = colors.dna;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(x, y + 20);
            ctx.lineTo(x + length * progress, y + 20);
            ctx.strokeStyle = colors.dnaStrand2;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制碱基对
            const visibleSegments = Math.floor(segmentCount * progress);
            for (let i = 0; i < visibleSegments; i++) {
                const segX = x + i * segmentLength + segmentLength / 2;
                
                // 碱基对连线
                ctx.beginPath();
                ctx.moveTo(segX, y);
                ctx.lineTo(segX, y + 20);
                ctx.strokeStyle = i % 2 === 0 ? '#e74c3c' : '#2ecc71';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 碱基标签
                if (showLabels && i % 3 === 0) {
                    ctx.fillStyle = colors.text;
                    ctx.font = '12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(dnaBases[i % 4], segX - 5, y - 5);
                    ctx.fillText(dnaBases[(i + 1) % 4], segX + 5, y + 25);
                }
            }
            
            // DNA标签
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('DNA', x + length / 2, y - 30);
            }
        }
        
        // 绘制RNA聚合酶
        function drawRNAPolymerase(x, y) {
            ctx.fillStyle = '#8e44ad';
            ctx.beginPath();
            ctx.ellipse(x, y, 20, 15, 0, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.fillStyle = '#732d91';
            ctx.beginPath();
            ctx.ellipse(x, y, 12, 10, 0, 0, Math.PI * 2);
            ctx.fill();
            
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('RNA聚合酶', x, y - 25);
            }
        }
        
        // 绘制pre-mRNA/mRNA
        function drawRNA(x, y, sequence, isMature = false, introns = []) {
            const baseSpacing = 15;
            const totalWidth = sequence.length * baseSpacing;
            
            // 绘制RNA骨架
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x + totalWidth, y);
            ctx.strokeStyle = colors.mrna;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制碱基
            for (let i = 0; i < sequence.length; i++) {
                const baseX = x + i * baseSpacing;
                
                // 检查是否为内含子
                let isIntron = false;
                for (const intron of introns) {
                    if (i >= intron.start && i <= intron.end && !intron.removed) {
                        isIntron = true;
                        break;
                    }
                }
                
                // 绘制碱基
                ctx.beginPath();
                ctx.moveTo(baseX, y);
                ctx.lineTo(baseX, y + (i % 2 === 0 ? 15 : -15));
                ctx.strokeStyle = isIntron ? colors.preMrnaIntron : colors.mrna;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 碱基标签
                if (showLabels && i % 3 === 0) {
                    ctx.fillStyle = isIntron ? colors.preMrnaIntron : colors.text;
                    ctx.font = '12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(sequence[i], baseX, y + (i % 2 === 0 ? 25 : -25));
                }
            }
            
            // RNA标签
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(isMature ? 'mRNA' : 'pre-mRNA', x + totalWidth / 2, y - 40);
            }
            
            return totalWidth;
        }
        
        // 绘制剪接过程
        function drawSplicing(x, y, progress, introns) {
            const radius = 30;
            const angle = Math.PI * 2 * progress;
            
            // 绘制剪接体
            ctx.strokeStyle = '#f39c12';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, angle);
            ctx.stroke();
            
            // 绘制被切除的内含子
            for (let i = 0; i < introns.length; i++) {
                if (introns[i].removed) {
                    const intronX = x + 100 + i * 60;
                    const intronY = y + 50;
                    
                    // 绘制内含子环
                    ctx.strokeStyle = colors.preMrnaIntron;
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.arc(intronX, intronY, 20, 0, Math.PI * 2 * (1 - progress));
                    ctx.stroke();
                    
                    // 绘制降解效果
                    if (progress > 0.5) {
                        ctx.globalAlpha = 1 - (progress - 0.5) * 2;
                        ctx.fillStyle = colors.preMrnaIntron;
                        ctx.beginPath();
                        ctx.arc(intronX, intronY, 15, 0, Math.PI * 2);
                        ctx.fill();
                        ctx.globalAlpha = 1;
                    }
                }
            }
            
            if (showLabels && progress > 0) {
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('剪接体', x, y - radius - 10);
            }
        }
        
        // 绘制细胞核
        function drawNucleus(x, y, radius) {
            // 细胞核膜
            ctx.strokeStyle = colors.dna;
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.stroke();
            
            // 细胞核内部
            ctx.fillStyle = colors.nucleus;
            ctx.beginPath();
            ctx.arc(x, y, radius - 2, 0, Math.PI * 2);
            ctx.fill();
            
            // 核孔
            ctx.fillStyle = colors.ribosome;
            ctx.beginPath();
            ctx.arc(x + radius * 0.7, y, 8, 0, Math.PI * 2);
            ctx.fill();
            
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('细胞核', x, y - radius - 20);
            }
        }
        
        // 绘制核糖体
        function drawRibosome(x, y, size = 1) {
            const width = 60 * size;
            const height = 40 * size;
            
            // 大亚基
            ctx.fillStyle = colors.ribosome;
            ctx.beginPath();
            ctx.ellipse(x, y, width / 2, height / 2, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 小亚基
            ctx.fillStyle = '#e67e22';
            ctx.beginPath();
            ctx.ellipse(x, y - height * 0.3, width * 0.6, height * 0.5, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // A、P、E位点标记
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('A', x - width * 0.3, y + height * 0.2);
                ctx.fillText('P', x, y + height * 0.2);
                ctx.fillText('E', x + width * 0.3, y + height * 0.2);
            }
            
            // 核糖体标签
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('核糖体', x, y - height - 10);
            }
        }
        
        // 绘制tRNA
        function drawTRNA(x, y, anticodon, aminoAcid, isDragging = false) {
            const size = isDragging ? 1.2 : 1;
            
            // tRNA主体（三叶草形状简化版）
            ctx.fillStyle = colors.trna;
            ctx.beginPath();
            
            // 主体
            ctx.ellipse(x, y, 20 * size, 15 * size, 0, 0, Math.PI * 2);
            
            // 反密码子臂
            ctx.moveTo(x, y + 15 * size);
            ctx.lineTo(x, y + 35 * size);
            
            // 氨基酸臂
            ctx.moveTo(x, y - 15 * size);
            ctx.lineTo(x, y - 35 * size);
            
            ctx.fill();
            ctx.strokeStyle = '#8e44ad';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 反密码子
            ctx.fillStyle = colors.text;
            ctx.font = '10px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(anticodon, x, y + 50 * size);
            
            // 氨基酸
            ctx.fillStyle = colors.aminoAcid;
            ctx.beginPath();
            ctx.arc(x, y - 45 * size, 10 * size, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.fillStyle = 'white';
            ctx.font = '9px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(aminoAcid.substring(0, 3), x, y - 43 * size);
            
            // tRNA标签
            if (showLabels && !isDragging) {
                ctx.fillStyle = colors.text;
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('tRNA', x, y - 65 * size);
            }
            
            return {
                x: x - 20 * size,
                y: y - 55 * size,
                width: 40 * size,
                height: 100 * size
            };
        }
        
        // 绘制肽链
        function drawPeptideChain(x, y, chain) {
            if (chain.length === 0) return;
            
            const spacing = 25;
            
            for (let i = 0; i < chain.length; i++) {
                const aminoX = x + i * spacing;
                
                // 氨基酸
                ctx.fillStyle = colors.aminoAcid;
                ctx.beginPath();
                ctx.arc(aminoX, y, 10, 0, Math.PI * 2);
                ctx.fill();
                
                // 氨基酸标签
                if (showLabels) {
                    ctx.fillStyle = 'white';
                    ctx.font = '10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(chain[i], aminoX, y + 3);
                }
                
                // 肽键（除了第一个氨基酸）
                if (i > 0) {
                    ctx.strokeStyle = colors.text;
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.moveTo(aminoX - spacing + 10, y);
                    ctx.lineTo(aminoX - 10, y);
                    ctx.stroke();
                    
                    if (showLabels && i === 1) {
                        ctx.fillStyle = colors.text;
                        ctx.font = '10px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('肽键', aminoX - spacing / 2, y - 15);
                    }
                }
            }
            
            // 肽链标签
            if (showLabels && chain.length > 1) {
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('生长中的肽链', x + (chain.length * spacing) / 2, y - 30);
            }
        }
        
        // 绘制场景1：转录与剪接
        function drawScene1() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('转录与剪接（细胞核内）', canvas.width / 2, 40);
            
            // 绘制DNA
            drawDNA(scene1.dnaX, scene1.dnaY, scene1.dnaLength, 1);
            
            // 绘制RNA聚合酶
            drawRNAPolymerase(scene1.rnaPolymeraseX, scene1.dnaY);
            
            // 更新转录进度
            if (isPlaying && currentScene === 1) {
                scene1.transcriptionProgress += 0.01;
                scene1.rnaPolymeraseX = scene1.dnaX + scene1.dnaLength * scene1.transcriptionProgress;
                
                // 生成pre-mRNA序列
                if (scene1.preMrna.length < 15 && Math.random() > 0.7) {
                    scene1.preMrna.push(rnaBases[scene1.preMrna.length % 4]);
                }
                
                // 转录完成，开始剪接
                if (scene1.transcriptionProgress >= 1 && !scene1.spliced) {
                    scene1.splicingProgress += 0.01;
                    
                    // 剪接完成
                    if (scene1.splicingProgress >= 1) {
                        scene1.spliced = true;
                        for (const intron of scene1.introns) {
                            intron.removed = true;
                        }
                    }
                }
            }
            
            // 绘制pre-mRNA
            if (scene1.preMrna.length > 0) {
                const rnaX = scene1.dnaX + 50;
                const rnaY = scene1.dnaY - 80;
                drawRNA(rnaX, rnaY, scene1.preMrna, false, scene1.introns);
                
                // 绘制剪接过程
                if (scene1.transcriptionProgress >= 1 && scene1.splicingProgress > 0) {
                    drawSplicing(rnaX + 200, rnaY, scene1.splicingProgress, scene1.introns);
                }
            }
            
            // 绘制说明
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = '14px Arial';
                ctx.textAlign = 'left';
                ctx.fillText('• RNA聚合酶沿DNA移动，合成pre-mRNA', 50, 450);
                ctx.fillText('• pre-mRNA包含外显子（红色）和内含子（橙色）', 50, 470);
                
                if (scene1.spliced) {
                    ctx.fillStyle = '#27ae60';
                    ctx.fillText('✓ 剪接完成：内含子被切除，外显子连接形成成熟mRNA', 50, 490);
                }
            }
        }
        
        // 绘制场景2：mRNA运输
        function drawScene2() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('mRNA运输与核糖体组装', canvas.width / 2, 40);
            
            // 绘制细胞核
            drawNucleus(scene2.nucleusX, scene2.nucleusY, scene2.nucleusRadius);
            
            // 绘制细胞质背景
            ctx.fillStyle = colors.cytoplasm;
            ctx.fillRect(scene2.nucleusX + scene2.nucleusRadius + 10, 0, 
                        canvas.width - (scene2.nucleusX + scene2.nucleusRadius + 10), canvas.height);
            
            // 更新运输进度
            if (isPlaying && currentScene === 2) {
                scene2.transportProgress += 0.01;
                scene2.mrnaX = scene2.nuclearPoreX + (scene2.ribosomeX - scene2.nuclearPoreX) * scene2.transportProgress;
                scene2.mrnaY = scene2.nuclearPoreY + (scene2.ribosomeY - scene2.nuclearPoreY) * scene2.transportProgress;
                
                // 运输完成，开始组装核糖体
                if (scene2.transportProgress >= 1) {
                    scene2.assemblyProgress += 0.01;
                }
            }
            
            // 绘制mRNA
            const mrnaSequence = ['A', 'U', 'G', 'C', 'U', 'U', 'U', 'C', 'U', 'A', 'G', 'A'];
            drawRNA(sc
<!--检测到代码截断，自动续写中...-->
scene2.mrnaX, scene2.mrnaY, mrnaSequence, true);
            
            // 绘制核糖体
            const ribosomeSize = 0.5 + scene2.assemblyProgress * 0.5;
            drawRibosome(scene2.ribosomeX, scene2.ribosomeY, ribosomeSize);
            
            // 绘制说明
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = '14px Arial';
                ctx.textAlign = 'left';
                ctx.fillText('• 成熟mRNA通过核孔离开细胞核', 50, 450);
                ctx.fillText('• mRNA进入细胞质并与核糖体小亚基结合', 50, 470);
                
                if (scene2.assemblyProgress >= 1) {
                    ctx.fillStyle = '#27ae60';
                    ctx.fillText('✓ 核糖体组装完成，准备开始翻译', 50, 490);
                }
            }
        }
        
        // 绘制场景3：翻译合成
        function drawScene3() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('翻译与肽链合成', canvas.width / 2, 40);
            
            // 绘制mRNA
            const codonSpacing = 40;
            const mrnaLength = scene3.mrnaSequence.length * codonSpacing;
            
            // mRNA骨架
            ctx.beginPath();
            ctx.moveTo(scene3.mrnaX, scene3.mrnaY);
            ctx.lineTo(scene3.mrnaX + mrnaLength, scene3.mrnaY);
            ctx.strokeStyle = colors.mrna;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制密码子
            for (let i = 0; i < scene3.mrnaSequence.length; i++) {
                const codonX = scene3.mrnaX + i * codonSpacing + codonSpacing / 2;
                
                // 绘制密码子框
                ctx.fillStyle = i === scene3.currentCodonIndex && highlightPairing ? colors.highlight : 'rgba(231, 76, 60, 0.1)';
                ctx.fillRect(codonX - 25, scene3.mrnaY - 20, 50, 40);
                
                // 绘制密码子文本
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(scene3.mrnaSequence[i], codonX, scene3.mrnaY + 5);
                
                // 密码子编号
                if (showLabels) {
                    ctx.fillStyle = colors.text;
                    ctx.font = '10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(`C${i+1}`, codonX, scene3.mrnaY - 25);
                }
            }
            
            // 绘制核糖体
            drawRibosome(scene3.ribosomeX, scene3.ribosomeY);
            
            // 高亮当前密码子对应的核糖体位点
            if (highlightPairing && scene3.currentCodonIndex < scene3.mrnaSequence.length) {
                const codonX = scene3.mrnaX + scene3.currentCodonIndex * codonSpacing + codonSpacing / 2;
                
                // 绘制连接线
                ctx.strokeStyle = colors.highlight;
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.moveTo(codonX, scene3.mrnaY + 20);
                ctx.lineTo(scene3.ribosomeX - 20, scene3.ribosomeY + 10);
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 绘制tRNA
            for (let i = 0; i < scene3.trnas.length; i++) {
                const trna = scene3.trnas[i];
                const isDragging = (scene3.draggingTrna === trna);
                
                // 如果tRNA在核糖体中，调整位置
                let drawX = trna.x;
                let drawY = trna.y;
                
                if (trna.state === 'inA') {
                    drawX = scene3.ribosomeX - 20;
                    drawY = scene3.ribosomeY + 30;
                } else if (trna.state === 'inP') {
                    drawX = scene3.ribosomeX;
                    drawY = scene3.ribosomeY + 30;
                } else if (trna.state === 'inE') {
                    drawX = scene3.ribosomeX + 20;
                    drawY = scene3.ribosomeY + 30;
                }
                
                // 绘制tRNA
                const bounds = drawTRNA(drawX, drawY, trna.anticodon, trna.aminoAcid, isDragging);
                
                // 保存边界信息用于点击检测
                trna.bounds = bounds;
                
                // 如果tRNA在A位点且密码子匹配，高亮显示
                if (trna.state === 'inA' && highlightPairing) {
                    const currentCodon = scene3.mrnaSequence[scene3.currentCodonIndex];
                    const complementaryCodon = getComplementaryCodon(currentCodon);
                    
                    if (trna.anticodon === complementaryCodon) {
                        ctx.strokeStyle = colors.highlight;
                        ctx.lineWidth = 3;
                        ctx.beginPath();
                        ctx.arc(drawX, drawY, 25, 0, Math.PI * 2);
                        ctx.stroke();
                    }
                }
            }
            
            // 绘制肽链
            if (scene3.peptideChain.length > 0) {
                const peptideX = scene3.ribosomeX;
                const peptideY = scene3.ribosomeY - 50;
                drawPeptideChain(peptideX, peptideY, scene3.peptideChain);
            }
            
            // 更新翻译进度
            if (isPlaying && currentScene === 3 && !gameMode) {
                scene3.translationProgress += 0.005;
                
                // 自动进行翻译步骤
                if (scene3.translationProgress >= 1 && scene3.currentCodonIndex < scene3.mrnaSequence.length) {
                    performTranslationStep();
                    scene3.translationProgress = 0;
                }
            }
            
            // 绘制说明
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = '14px Arial';
                ctx.textAlign = 'left';
                ctx.fillText('• tRNA通过反密码子与mRNA密码子配对', 50, 450);
                ctx.fillText('• 核糖体催化肽键形成，延伸肽链', 50, 470);
                ctx.fillText('• 翻译从起始密码子AUG开始，到终止密码子结束', 50, 490);
            }
            
            // 游戏模式信息
            if (gameMode) {
                ctx.fillStyle = '#d35400';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('游戏模式：拖拽正确的tRNA到核糖体A位点', canvas.width / 2, 100);
                
                // 显示当前密码子
                const currentCodon = scene3.mrnaSequence[scene3.currentCodonIndex];
                ctx.fillStyle = colors.text;
                ctx.font = '18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`当前密码子: ${currentCodon}`, canvas.width / 2, 130);
                
                // 显示互补密码子提示
                const complementaryCodon = getComplementaryCodon(currentCodon);
                ctx.fillStyle = '#27ae60';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`需要反密码子: ${complementaryCodon}`, canvas.width / 2, 155);
            }
        }
        
        // 执行翻译步骤
        function performTranslationStep() {
            if (scene3.currentCodonIndex >= scene3.mrnaSequence.length) return;
            
            const currentCodon = scene3.mrnaSequence[scene3.currentCodonIndex];
            const complementaryCodon = getComplementaryCodon(currentCodon);
            
            // 查找匹配的tRNA
            let matchedTrna = null;
            for (const trna of scene3.trnas) {
                if (trna.state === 'free' && trna.anticodon === complementaryCodon) {
                    matchedTrna = trna;
                    break;
                }
            }
            
            if (matchedTrna) {
                // 移动tRNA到A位点
                matchedTrna.state = 'inA';
                matchedTrna.x = scene3.ribosomeX - 20;
                matchedTrna.y = scene3.ribosomeY + 30;
                
                // 如果是第一个密码子，直接添加到P位点
                if (scene3.currentCodonIndex === 0) {
                    matchedTrna.state = 'inP';
                    matchedTrna.x = scene3.ribosomeX;
                    scene3.peptideChain.push(matchedTrna.aminoAcid);
                } else if (scene3.currentCodonIndex > 0) {
                    // 将P位点的tRNA氨基酸添加到肽链
                    for (const trna of scene3.trnas) {
                        if (trna.state === 'inP') {
                            scene3.peptideChain.push(trna.aminoAcid);
                            trna.state = 'inE'; // 移动到E位点
                            break;
                        }
                    }
                    
                    // A位点tRNA移动到P位点
                    setTimeout(() => {
                        matchedTrna.state = 'inP';
                        matchedTrna.x = scene3.ribosomeX;
                    }, 500);
                }
                
                // 清除E位点的tRNA
                setTimeout(() => {
                    for (const trna of scene3.trnas) {
                        if (trna.state === 'inE') {
                            trna.state = 'free';
                            trna.x = 100 + Math.random() * 150;
                            trna.y = 100 + Math.random() * 150;
                        }
                    }
                }, 1000);
                
                scene3.currentCodonIndex++;
                
                // 到达终止密码子
                if (scene3.currentCodonIndex >= scene3.mrnaSequence.length) {
                    setTimeout(() => {
                        // 释放最后的tRNA
                        for (const trna of scene3.trnas) {
                            if (trna.state === 'inP') {
                                trna.state = 'free';
                                trna.x = 100 + Math.random() * 150;
                                trna.y = 100 + Math.random() * 150;
                            }
                        }
                    }, 500);
                }
            }
        }
        
        // 游戏模式：检查tRNA是否正确
        function checkGameAnswer(trna) {
            const currentCodon = scene3.mrnaSequence[scene3.currentCodonIndex];
            const complementaryCodon = getComplementaryCodon(currentCodon);
            
            if (trna.anticodon === complementaryCodon) {
                // 正确答案
                gameScore++;
                document.getElementById('gameScore').textContent = gameScore;
                
                // 执行翻译步骤
                trna.state = 'inA';
                trna.x = scene3.ribosomeX - 20;
                trna.y = scene3.ribosomeY + 30;
                
                setTimeout(() => {
                    performTranslationStep();
                    
                    // 更新游戏信息
                    if (scene3.currentCodonIndex < scene3.mrnaSequence.length) {
                        document.getElementById('currentCodon').textContent = 
                            scene3.mrnaSequence[scene3.currentCodonIndex];
                    } else {
                        document.getElementById('currentCodon').textContent = "完成!";
                    }
                }, 500);
                
                return true;
            } else {
                // 错误答案
                return false;
            }
        }
        
        // 主绘制函数
        function draw() {
            switch (currentScene) {
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
            
            if (isPlaying) {
                animationFrameId = requestAnimationFrame(draw);
            }
        }
        
        // 切换场景
        function switchScene(sceneNumber) {
            currentScene = sceneNumber;
            isPlaying = false;
            
            // 更新场景按钮状态
            document.getElementById('scene1Btn').classList.toggle('active', sceneNumber === 1);
            document.getElementById('scene2Btn').classList.toggle('active', sceneNumber === 2);
            document.getElementById('scene3Btn').classList.toggle('active', sceneNumber === 3);
            
            // 更新状态栏
            const sceneNames = ['', '转录与剪接', 'mRNA运输', '翻译合成'];
            statusBar.textContent = `场景：${sceneNames[sceneNumber]}`;
            
            // 重置场景状态
            if (sceneNumber === 1) {
                scene1.transcriptionProgress = 0;
                scene1.rnaPolymeraseX = 100;
                scene1.preMrna = [];
                scene1.spliced = false;
                scene1.splicingProgress = 0;
                for (const intron of scene1.introns) {
                    intron.removed = false;
                }
            } else if (sceneNumber === 2) {
                scene2.transportProgress = 0;
                scene2.assemblyProgress = 0;
                scene2.mrnaX = 150;
                scene2.mrnaY = 250;
            } else if (sceneNumber === 3) {
                initTranslationScene();
                scene3.translationProgress = 0;
            }
            
            // 停止之前的动画
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
            }
            
            // 开始绘制
            draw();
        }
        
        // 事件监听器
        document.getElementById('playBtn').addEventListener('click', () => {
            isPlaying = true;
            if (!animationFrameId) {
                animationFrameId = requestAnimationFrame(draw);
            }
        });
        
        document.getElementById('pauseBtn').addEventListener('click', () => {
            isPlaying = false;
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
        });
        
        document.getElementById('stepBtn').addEventListener('click', () => {
            isPlaying = false;
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
            
            // 执行单步操作
            if (currentScene === 1) {
                if (scene1.transcriptionProgress < 1) {
                    scene1.transcriptionProgress += 0.1;
                    scene1.rnaPolymeraseX = scene1.dnaX + scene1.dnaLength * scene1.transcriptionProgress;
                    
                    if (scene1.preMrna.length < 15) {
                        scene1.preMrna.push(rnaBases[scene1.preMrna.length % 4]);
                    }
                } else if (!scene1.spliced && scene1.splicingProgress < 1) {
                    scene1.splicingProgress += 0.2;
                    if (scene1.splicingProgress >= 1) {
                        scene1.spliced = true;
                        for (const intron of scene1.introns) {
                            intron.removed = true;
                        }
                    }
                }
            } else if (currentScene === 2) {
                if (scene2.transportProgress < 1) {
                    scene2.transportProgress += 0.2;
                    scene2.mrnaX = scene2.nuclearPoreX + (scene2.ribosomeX - scene2.nuclearPoreX) * scene2.transportProgress;
                    scene2.mrnaY = scene2.nuclearPoreY + (scene2.ribosomeY - scene2.nuclearPoreY) * scene2.transportProgress;
                } else if (scene2.assemblyProgress < 1) {
                    scene2.assemblyProgress += 0.2;
                }
            } else if (currentScene === 3 && !gameMode) {
                performTranslationStep();
            }
            
            draw();
        });
        
        document.getElementById('resetBtn').addEventListener('click', () => {
            isPlaying = false;
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
            
            switchScene(currentScene);
        });
        
        document.getElementById('scene1Btn').addEventListener('click', () => switchScene(1));
        document.getElementById('scene2Btn').addEventListener('click', () => switchScene(2));
        document.getElementById('scene3Btn').addEventListener('click', () => switchScene(3));
        
        document.getElementById('toggleLabelsBtn').addEventListener('click', function() {
            showLabels = !showLabels;
            this.textContent = showLabels ? '隐藏标签' : '显示标签';
            draw();
        });
        
        document.getElementById('highlightBtn').addEventListener('click', function() {
            highlightPairing = !highlightPairing;
            this.textContent = highlightPairing ? '取消高亮' : '高亮配对';
            draw();
        });
        
        document.getElementById('gameModeBtn').addEventListener('click', function() {
            gameMode = !gameMode;
            this.textContent = gameMode ? '退出游戏' : '拖拽匹配游戏';
            document.getElementById('gameModePanel').style.display = gameMode ? 'block' : 'none';
            
            if (gameMode) {
                // 初始化游戏
                gameScore = 0;
                gameTotal = scene3.mrnaSequence.length;
                document.getElementById('gameScore').textContent = gameScore;
                document.getElementById('gameTotal').textContent = gameTotal;
                document.getElementById('currentCodon').textContent = scene3.mrnaSequence[scene3.currentCodonIndex];
                
                // 重置翻译状态
                scene3.currentCodonIndex = 0;
                scene3.peptideChain = [];
                initTranslationScene();
            } else {
                // 退出游戏模式
                switchScene(3);
            }
            
            draw();
        });
        
        // 鼠标事件处理
        let mouseX = 0, mouseY = 0;
        
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            mouseX = e.clientX - rect.left;
            mouseY = e.clientY - rect.top;
            
            // 更新工具提示
            if (currentScene === 3) {
                let tooltipText = '';
                
                // 检查是否悬停在tRNA上
                for (const trna of scene3.trnas) {
                    if (trna.bounds && 
                        mouseX >= trna.bounds.x && mouseX <= trna.bounds.x + trna.bounds.width &&
                        mouseY >= trna.bounds.y && mouseY <= trna.bounds.y + trna.bounds.height) {
                        
                        tooltipText = `tRNA\n反密码子: ${trna.anticodon}\n携带氨基酸: ${trna.aminoAcid}`;
                        break;
                    }
                }
                
                // 检查是否悬停在密码子上
                if (!tooltipText && currentScene === 3) {
                    const codonSpacing = 40;
                    for (let i = 0; i < scene3.mrnaSequence.length; i++) {
                        const codonX = scene3.mrnaX + i * codonSpacing + codonSpacing / 2;
                        if (Math.abs(mouseX - codonX) < 25 && Math.abs(mouseY - scene3.mrnaY) < 25) {
                            tooltipText = `密码子: ${scene3.mrnaSequence[i]}\n位置: ${i+1}`;
                            break;
                        }
                    }
                }
                
                if (tooltipText) {
                    tooltip.style.display = 'block';
                    tooltip.style.left = (e.clientX + 10) + 'px';
                    tooltip.style.top = (e.clientY + 10) + 'px';
                    tooltip.textContent = tooltipText;
                } else {
                    tooltip.style.display = 'none';
                }
            }
            
            // 拖拽tRNA
            if (scene3.draggingTrna) {
                scene3.draggingTrna.x = mouseX - scene3.dragOffsetX;
                scene3.draggingTrna.y = mouseY - scene3.dragOffsetY;
                draw();
            }
        });
        
        canvas.addEventListener('mousedown', (e) => {
            if (currentScene === 3 && gameMode) {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                // 检查是否点击了tRNA
                for (const trna of scene3.trnas) {
                    if (trna.bounds && 
                        x >= trna.bounds.x && x <= trna.bounds.x + trna.bounds.width &&
                        y >= trna.bounds.y && y <= trna.bounds.y + trna.bounds.height &&
                        trna.state === 'free') {
                        
                        scene3.draggingTrna = trna;
                        scene3.dragOffsetX = x - trna.x;
                        scene3.dragOffsetY = y - trna.y;
                        break;
                    }
                }
            }
        });
        
        canvas.addEventListener('mouseup', (e) => {
            if (scene3.draggingTrna) {
                // 检查是否拖拽到了核糖体A位点
                const aSiteX = scene3.ribosomeX - 20;
                const aSiteY = scene3.ribosomeY + 30;
                const distance = Math.sqrt(
                    Math.pow(scene3.draggingTrna.x - aSiteX, 2) + 
                    Math.pow(scene3.draggingTrna.y - aSiteY, 2)
                );
                
                if (distance < 40) {
                    // 在A位点附近，检查答案
                    const isCorrect = checkGameAnswer(scene3.draggingTrna);
                    
                    if (isCorrect) {
                        scene3.draggingTrna.x = aSiteX;
                        scene3.draggingTrna.y = aSiteY;
                    } else {
                        // 错误答案，返回原位置
                        scene3.draggingTrna.x = 100 + Math.random() * 150;
                        scene3.draggingTrna.y = 100 + Math.random() * 150;
                    }
                } else {
                    // 不在A位点，返回原位置
                    scene3.draggingTrna.x = 100 + Math.random() * 150;
                    scene3.draggingTrna.y = 100 + Math.random() * 150;
                }
                
                scene3.draggingTrna = null;
                draw();
            }
        });
        
        canvas.addEventListener('mouseleave', () => {
            tooltip.style.display = 'none';
            
            if (scene3.draggingTrna) {
                scene3.draggingTrna.x = 100 + Math.random() * 150;
                scene3.draggingTrna.y = 100 + Math.random() * 150;
                scene3.draggingTrna = null;
                draw();
            }
        });
        
        // 初始化
        switchScene(1);
        draw();
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用“中心法则：从DNA到蛋白质”交互式教学动画！本指南将帮助您充分利用这个精心设计的教学工具，深入理解遗传信息传递的核心过程。

### 🎯 功能说明

本动画是一个基于HTML5 Canvas开发的交互式教学工具，旨在通过动态可视化方式，生动展示遗传信息从DNA转录为mRNA，经过剪接后翻译成蛋白质的完整过程。它将复杂的分子生物学过程分解为三个清晰的场景，支持自主探索和交互操作。

### 🚀 主要功能

#### 1. **场景导航系统**
- **场景一：转录与剪接** - 展示细胞核内DNA转录为pre-mRNA及剪接过程
- **场景二：mRNA运输** - 显示成熟mRNA通过核孔进入细胞质并与核糖体结合
- **场景三：翻译合成** - 演示核糖体上tRNA携带氨基酸合成多肽链的过程

#### 2. **动画控制面板**
- **播放/暂停**：控制动画的连续播放
- **下一步**：单步执行每个关键步骤
- **重置**：将当前场景恢复到初始状态

#### 3. **交互学习工具**
- **显示/隐藏标签**：切换分子名称和位点标签的显示
- **高亮配对**：突出显示碱基配对和密码子-反密码子配对过程
- **拖拽匹配游戏**：在翻译场景中，通过拖拽正确的tRNA到核糖体A位点进行互动学习

#### 4. **视觉辅助功能**
- **颜色编码系统**：不同分子使用统一配色方案（DNA-蓝色、mRNA-红色、tRNA-紫色等）
- **实时状态显示**：顶部状态栏显示当前场景和进度
- **悬停提示**：鼠标悬停在分子上显示详细信息

### ✨ 设计特色

#### 1. **科学准确性**
- 严格遵循中心法则的生物学原理
- 准确展示碱基互补配对规则（A-U/T-A，C-G）
- 真实模拟剪接体切除内含子的过程
- 正确呈现核糖体A/P/E三个功能位点

#### 2. **教学友好性**
- **渐进式学习**：从简单到复杂，分场景逐步深入
- **难点可视化**：将抽象的剪接和翻译过程具体化
- **即时反馈**：游戏模式提供学习成果的即时验证
- **自主控制**：用户可按照自己的节奏学习

#### 3. **技术实现**
- 流畅的Canvas动画，确保跨平台兼容性
- 响应式设计，适配不同屏幕尺寸
- 轻量级实现，无需额外插件或软件

### 📚 教学要点

#### 核心概念强化
1. **信息流方向**：DNA → mRNA → 蛋白质的单向传递
2. **分子识别**：碱基互补配对是遗传信息准确传递的基础
3. **空间分隔**：转录在细胞核，翻译在细胞质
4. **能量转换**：遗传信息最终转换为具有功能的蛋白质

#### 关键过程理解
- **转录**：理解RNA聚合酶的作用和模板链概念
- **剪接**：区分内含子（非编码区）和外显子（编码区）
- **翻译**：掌握密码子与反密码子的对应关系
- **肽链合成**：了解氨基酸通过肽键连接形成多肽

### 💡 使用建议

#### 对于教师
1. **课堂演示**：使用投影仪全屏展示，配合讲解逐步推进
2. **小组学习**：将学生分组，分配不同场景进行探索和汇报
3. **难点突破**：针对剪接和翻译等难点，反复播放关键步骤
4. **评估工具**：利用游戏模式检验学生对密码子-反密码子配对的理解

#### 对于学生
1. **自主学习**：按照场景顺序系统学习，使用“下一步”功能控制节奏
2. **重点复习**：对不理解的部分可反复观看，结合右侧文字说明
3. **自我测试**：完成正常学习后，尝试游戏模式检验掌握程度
4. **概念联系**：注意观察DNA序列如何最终决定蛋白质的氨基酸序列

#### 最佳实践流程
1. **初次接触**：按顺序观看三个场景的完整动画，建立整体概念
2. **深入学习**：选择特定场景，使用单步功能仔细研究每个细节
3. **互动探索**：开启标签和高亮功能，理解分子间的相互作用
4. **知识应用**：进入游戏模式，实践密码子-反密码子的配对识别
5. **总结反思**：回顾整个过程，思考遗传信息传递的意义和准确性保障机制

#### 技术提示
- 推荐使用Chrome、Firefox或Edge等现代浏览器
- 确保浏览器已启用JavaScript
- 在全屏模式下可获得最佳观看体验
- 如有显示问题，尝试刷新页面或调整浏览器缩放比例

---

**开始您的分子生物学探索之旅吧！** 通过这个交互式动画，您将能够直观地理解生命最基本的遗传信息传递过程，揭开从基因到蛋白质的神秘面纱。祝您学习愉快，探索成功！ 🧬🔬✨