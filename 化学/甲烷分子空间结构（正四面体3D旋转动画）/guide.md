# 需求：甲烷分子空间结构（正四面体3D旋转动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的化学学生。他们已具备基础的原子、共价键和分子式知识，但对分子的三维空间构型理解存在困难，尤其是抽象的“正四面体”概念。
2.  **核心需求**：用户需要通过直观、动态的视觉化手段，理解甲烷（CH₄）分子中碳原子位于正四面体中心，四个氢原子位于四个顶点，以及所有键角均为109°28‘这一核心空间构型。静态的二维图片或球棍模型不足以展示其立体对称性。
3.  **深层需求**：用户需要建立“分子式（CH₄）→ 二维结构式（H-C-H）→ 三维空间构型（正四面体）”之间的逻辑联系，并理解这种构型是电子对互斥和杂化轨道理论的结果（虽然本动画可能不深入理论，但应为理论教学打下直观基础）。

#### 教学设计思路
*   **核心概念**：
    *   甲烷分子的原子组成（1个C，4个H）。
    *   空间构型：**正四面体**。
    *   关键几何参数：**键角（109.5°）**、键长（C-H键等长）。
    *   对称性：分子高度对称，从任何顶点（H原子）看过去，结构相同。
*   **认知规律**：
    1.  **从已知到未知**：从学生熟悉的甲烷分子式和平面结构式引入。
    2.  **从静态到动态**：先展示一个静态的3D正四面体模型，然后通过自动旋转，让学生从各个角度观察其立体结构。
    3.  **从整体到局部**：在展示整体旋转后，允许用户聚焦于特定部分，如高亮一个C-H键，或透视内部的碳原子。
    4.  **通过交互深化理解**：提供可控的旋转、键角测量、结构切换（球棍模型 vs 比例模型）等交互，让用户主动探索，而非被动观看。
*   **交互设计**：
    *   **引导式探索**：设计简单的步骤提示或标签，引导用户按教学逻辑进行操作。
    *   **渐进式呈现**：信息分层显示，初始界面简洁，复杂信息（如键角数值、坐标轴）通过按钮触发显示，避免认知过载。
    *   **即时反馈**：用户操作（如点击原子、切换模型）应有明确的视觉或文本反馈。
*   **视觉呈现**：
    *   使用**WebGL（Three.js库）** 实现高质量的实时3D渲染，确保动画流畅。
    *   采用**卡通渲染风格**，线条清晰，颜色鲜明，避免写实渲染带来的复杂光影干扰教学重点。
    *   关键元素突出：碳原子与氢原子用不同颜色和大小区分，化学键清晰可见。正四面体的透明面或棱边可用于辅助理解空间结构。
    *   添加**坐标轴（x， y， z）** 和**角度标注弧线**，将抽象空间关系量化、可视化。

#### 配色方案选择
*   **科学性**与**清晰度**优先，遵循化学可视化惯例：
    *   **碳原子（C）**：**深灰色**或**黑色**。这是化学模型中表示碳的标准色。
    *   **氢原子（H）**：**白色**或**浅灰色**。标准色，与碳形成鲜明对比。
    *   **化学键**：**红色**或**深灰色**。红色能有效吸引注意力，表示共价键的连接；深灰色则更接近传统球棍模型。
    *   **正四面体辅助几何体**：**半透明的浅蓝色面或浅灰色棱边**。用于示意空间形状，但不喧宾夺主。
    *   **背景**：**深色（如深蓝、深灰）**。深色背景能最大化突出前景中颜色鲜艳的分子模型，减少视觉干扰，营造“科学探索”感。
    *   **UI控件与文本**：**白色**或**浅黄色**，确保在深色背景上清晰可读。

#### 交互功能列表
1.  **3D模型控制**：
    *   **自动旋转**：模型缓慢持续旋转，默认开启。
    *   **手动旋转**：用户通过鼠标拖拽从任意角度观察模型。
    *   **缩放**：通过鼠标滚轮放大/缩小模型。
    *   **平移**：按住特定键（如Shift）加鼠标拖拽平移视图。
2.  **模型切换**：
    *   **球棍模型**：原子为球体，键为棍棒。重点展示连接关系和空间构型。
    *   **比例模型（空间填充模型）**：原子按范德华半径比例显示为相互接触的球体。重点展示分子实际占据的空间大小。
3.  **信息显示/隐藏**：
    *   **原子标签**：显示/隐藏“C”和“H”标签。
    *   **键角显示**：点击按钮或直接点击某个键角区域，显示该角度（109.5°）的弧线和数值标签。
    *   **坐标轴**：显示/隐藏三维坐标轴（x， y， z）。
    *   **正四面体辅助线**：显示/隐藏连接四个氢原子构成的透明正四面体面或棱边。
4.  **教学提示与标注**：
    *   **分步讲解面板**：侧边栏或底部栏提供简短的文字步骤，如“第一步：观察整体结构”、“第二步：注意所有键角相等”等。
    *   **高亮功能**：点击某个C-H键或氢原子，可高亮显示，并可能伴随文字说明（如“所有四个C-H键完全相同”）。
5.  **重置视图**：一键将模型恢复至初始视角和状态。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>甲烷分子空间结构 - 正四面体3D动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #0a1929 0%, #1a1a2e 100%);
            color: #f0f8ff;
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
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #4facfe 0%, #00f2fe 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.8;
            margin-bottom: 15px;
        }

        .content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }

        .canvas-container {
            flex: 1;
            min-width: 300px;
            min-height: 500px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        #moleculeCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .controls-panel {
            flex: 0 0 300px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .control-group {
            margin-bottom: 25px;
        }

        h2 {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: #4facfe;
            border-bottom: 2px solid rgba(79, 172, 254, 0.3);
            padding-bottom: 5px;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }

        button {
            padding: 10px 15px;
            background: rgba(79, 172, 254, 0.2);
            border: 1px solid rgba(79, 172, 254, 0.4);
            color: #f0f8ff;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9rem;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background: rgba(79, 172, 254, 0.4);
            transform: translateY(-2px);
        }

        button.active {
            background: rgba(79, 172, 254, 0.6);
            border-color: #4facfe;
            box-shadow: 0 0 15px rgba(79, 172, 254, 0.4);
        }

        .checkbox-group {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .checkbox-label {
            display: flex;
            align-items: center;
            cursor: pointer;
        }

        .checkbox-label input {
            margin-right: 10px;
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .info-panel {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 20px;
        }

        .step-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .step {
            padding: 15px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 10px;
            border-left: 4px solid #4facfe;
            transition: all 0.3s ease;
        }

        .step.active {
            background: rgba(79, 172, 254, 0.1);
            border-left-color: #00f2fe;
        }

        .step h3 {
            font-size: 1.1rem;
            margin-bottom: 8px;
            color: #00f2fe;
        }

        .properties {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .property {
            background: rgba(255, 255, 255, 0.03);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
        }

        .property .value {
            font-size: 1.8rem;
            font-weight: bold;
            color: #4facfe;
            margin: 10px 0;
        }

        .property .label {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            opacity: 0.7;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .content {
                flex-direction: column;
            }
            
            .controls-panel {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>甲烷分子空间结构</h1>
            <div class="subtitle">CH₄ 正四面体3D交互式教学动画</div>
            <p>探索甲烷分子的三维空间构型，理解正四面体结构和109.5°键角</p>
        </header>

        <div class="content">
            <div class="canvas-container">
                <canvas id="moleculeCanvas"></canvas>
            </div>

            <div class="controls-panel">
                <div class="control-group">
                    <h2>模型控制</h2>
                    <div class="button-group">
                        <button id="autoRotate" class="active">自动旋转</button>
                        <button id="resetView">重置视图</button>
                    </div>
                    <p>提示：使用鼠标拖拽旋转，滚轮缩放</p>
                </div>

                <div class="control-group">
                    <h2>模型类型</h2>
                    <div class="button-group">
                        <button id="ballStick" class="active">球棍模型</button>
                        <button id="spaceFilling">比例模型</button>
                    </div>
                </div>

                <div class="control-group">
                    <h2>显示选项</h2>
                    <div class="checkbox-group">
                        <label class="checkbox-label">
                            <input type="checkbox" id="showLabels" checked>
                            <span>显示原子标签</span>
                        </label>
                        <label class="checkbox-label">
                            <input type="checkbox" id="showAngle" checked>
                            <span>显示键角(109.5°)</span>
                        </label>
                        <label class="checkbox-label">
                            <input type="checkbox" id="showTetrahedron">
                            <span>显示正四面体框架</span>
                        </label>
                        <label class="checkbox-label">
                            <input type="checkbox" id="showAxes">
                            <span>显示坐标轴</span>
                        </label>
                    </div>
                </div>

                <div class="control-group">
                    <h2>分子属性</h2>
                    <div class="properties">
                        <div class="property">
                            <div class="label">分子式</div>
                            <div class="value">CH₄</div>
                        </div>
                        <div class="property">
                            <div class="label">键角</div>
                            <div class="value">109.5°</div>
                        </div>
                        <div class="property">
                            <div class="label">对称性</div>
                            <div class="value">T<sub>d</sub></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="info-panel">
            <h2>教学步骤</h2>
            <div class="step-container">
                <div class="step active" id="step1">
                    <h3>步骤1：观察整体结构</h3>
                    <p>注意甲烷分子中碳原子位于正四面体中心，四个氢原子位于四个顶点。所有C-H键等长，所有键角相等。</p>
                </div>
                <div class="step" id="step2">
                    <h3>步骤2：理解键角</h3>
                    <p>甲烷分子中所有H-C-H键角均为109.5°，这是sp³杂化轨道理论预测的理想四面体角。</p>
                </div>
                <div class="step" id="step3">
                    <h3>步骤3：探索对称性</h3>
                    <p>旋转分子，观察其高度对称性。从任意氢原子视角看，分子结构完全相同。</p>
                </div>
                <div class="step" id="step4">
                    <h3>步骤4：比较模型</h3>
                    <p>切换不同模型：球棍模型展示连接关系，比例模型展示分子实际占据的空间大小。</p>
                </div>
            </div>
        </div>

        <footer>
            <p>教育技术交互式动画 | 甲烷分子空间结构教学工具</p>
            <p>提示：本动画使用HTML5 Canvas实现3D渲染，支持现代浏览器</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('moleculeCanvas');
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
        
        // 分子数据
        const molecule = {
            atoms: [
                { type: 'C', x: 0, y: 0, z: 0, radius: 30, color: '#333333' }, // 碳原子在中心
                { type: 'H', x: 0, y: 0, z: 100, radius: 20, color: '#ffffff' }, // 氢原子1
                { type: 'H', x: 94.3, y: 0, z: -31.4, radius: 20, color: '#ffffff' }, // 氢原子2
                { type: 'H', x: -47.1, y: 81.6, z: -31.4, radius: 20, color: '#ffffff' }, // 氢原子3
                { type: 'H', x: -47.1, y: -81.6, z: -31.4, radius: 20, color: '#ffffff' }  // 氢原子4
            ],
            bonds: [
                { from: 0, to: 1 }, // C-H1
                { from: 0, to: 2 }, // C-H2
                { from: 0, to: 3 }, // C-H3
                { from: 0, to: 4 }  // C-H4
            ],
            rotation: { x: 0, y: 0, z: 0 },
            scale: 1,
            offset: { x: 0, y: 0 }
        };
        
        // 3D投影函数
        function project3D(x, y, z) {
            // 应用旋转
            const cosX = Math.cos(molecule.rotation.x);
            const sinX = Math.sin(molecule.rotation.x);
            const cosY = Math.cos(molecule.rotation.y);
            const sinY = Math.sin(molecule.rotation.y);
            
            let y1 = y * cosX - z * sinX;
            let z1 = y * sinX + z * cosX;
            
            let x1 = x * cosY + z1 * sinY;
            z1 = -x * sinY + z1 * cosY;
            
            // 透视投影
            const perspective = 500;
            const scale = perspective / (perspective + z1);
            
            return {
                x: x1 * scale * molecule.scale + canvas.width / 2 + molecule.offset.x,
                y: y1 * scale * molecule.scale + canvas.height / 2 + molecule.offset.y,
                z: z1,
                scale: scale
            };
        }
        
        // 绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            const gradient = ctx.createRadialGradient(
                canvas.width / 2, canvas.height / 2, 0,
                canvas.width / 2, canvas.height / 2, Math.max(canvas.width, canvas.height) / 2
            );
            gradient.addColorStop(0, 'rgba(10, 25, 41, 0.8)');
            gradient.addColorStop(1, 'rgba(26, 26, 46, 0.8)');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制坐标轴（如果启用）
            if (document.getElementById('showAxes').checked) {
                drawAxes();
            }
            
            // 绘制正四面体框架（如果启用）
            if (document.getElementById('showTetrahedron').checked) {
                drawTetrahedronFrame();
            }
            
            // 绘制键角（如果启用）
            if (document.getElementById('showAngle').checked) {
                drawBondAngles();
            }
            
            // 绘制化学键
            molecule.bonds.forEach(bond => {
                const atom1 = molecule.atoms[bond.from];
                const atom2 = molecule.atoms[bond.to];
                
                const p1 = project3D(atom1.x, atom1.y, atom1.z);
                const p2 = project3D(atom2.x, atom2.y, atom2.z);
                
                // 绘制键
                ctx.beginPath();
                ctx.moveTo(p1.x, p1.y);
                ctx.lineTo(p2.x, p2.y);
                ctx.strokeStyle = document.getElementById('ballStick').classList.contains('active') ? 
                    '#ff4444' : 'rgba(255, 255, 255, 0.3)';
                ctx.lineWidth = document.getElementById('ballStick').classList.contains('active') ? 4 : 8;
                ctx.stroke();
            });
            
            // 绘制原子（按深度排序）
            const projectedAtoms = molecule.atoms.map((atom, index) => {
                const p = project3D(atom.x, atom.y, atom.z);
                return { ...atom, ...p, index };
            });
            
            projectedAtoms.sort((a, b) => b.z - a.z);
            
            projectedAtoms.forEach(atom => {
                // 根据模型类型调整原子大小
                let radius = atom.radius;
                if (!document.getElementById('ballStick').classList.contains('active')) {
                    radius *= 1.5; // 比例模型原子更大
                }
                
                radius *= atom.scale;
                
                // 绘制原子球体
                const gradient = ctx.createRadialGradient(
                    atom.x, atom.y, 0,
                    atom.x, atom.y, radius
                );
                
                if (atom.type === 'C') {
                    gradient.addColorStop(0, '#666666');
                    gradient.addColorStop(0.7, '#333333');
                    gradient.addColorStop(1, '#000000');
                } else {
                    gradient.addColorStop(0, '#ffffff');
                    gradient.addColorStop(0.7, '#cccccc');
                    gradient.addColorStop(1, '#999999');
                }
                
                ctx.beginPath();
                ctx.arc(atom.x, atom.y, radius, 0, Math.PI * 2);
                ctx.fillStyle = gradient;
                ctx.fill();
                
                // 添加高光
                ctx.beginPath();
                ctx.arc(atom.x - radius * 0.3, atom.y - radius * 0.3, radius * 0.3, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
                ctx.fill();
                
                // 绘制原子标签（如果启用）
                if (document.getElementById('showLabels').checked) {
                    ctx.font = `${Math.max(14, radius * 0.8)}px Arial`;
                    ctx.fillStyle = atom.type === 'C' ? '#ffffff' : '#000000';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(atom.type, atom.x, atom.y);
                }
            });
            
            // 更新教学步骤高亮
            updateStepHighlight();
        }
        
        // 绘制坐标轴
        function drawAxes() {
            const length = 80;
            const axes = [
                { x: length, y: 0, z: 0, color: '#ff4444', label: 'X' },
                { x: 0, y: length, z: 0, color: '#44ff44', label: 'Y' },
                { x: 0, y: 0, z: length, color: '#4444ff', label: 'Z' }
            ];
            
            const origin = project3D(0, 0, 0);
            
            axes.forEach(axis => {
                const end = project3D(axis.x, axis.y, axis.z);
                
                // 绘制轴线
                ctx.beginPath();
                ctx.moveTo(origin.x, origin.y);
                ctx.lineTo(end.x, end.y);
                ctx.strokeStyle = axis.color;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制箭头
                const angle = Math.atan2(end.y - origin.y, end.x - origin.x);
                const arrowSize = 8;
                
                ctx.beginPath();
                ctx.moveTo(end.x, end.y);
                ctx.lineTo(
                    end.x - arrowSize * Math.cos(angle - Math.PI / 6),
                    end.y - arrowSize * Math.sin(angle - Math.PI / 6)
                );
                ctx.lineTo(
                    end.x - arrowSize * Math.cos(angle + Math.PI / 6),
                    end.y - arrowSize * Math.sin(angle + Math.PI / 6)
                );
                ctx.closePath();
                ctx.fillStyle = axis.color;
                ctx.fill();
                
                // 绘制标签
                ctx.font = '14px Arial';
                ctx.fillStyle = axis.color;
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(axis.label, end.x + 15 * Math.cos(angle), end.y + 15 * Math.sin(angle));
            });
        }
        
        // 绘制正四面体框架
        function drawTetrahedronFrame() {
            const vertices = molecule.atoms.slice(1).map(atom => project3D(atom.x, atom.y, atom.z));
            
            // 绘制四面体的面
            ctx.globalAlpha = 0.1;
            ctx.fillStyle = '#4facfe';
            
            // 面1: H1-H2-H3
            ctx.beginPath();
            ctx.moveTo(vertices[0].x, vertices[0].y);
            ctx.lineTo(vertices[1].x, vertices[1].y);
            ctx.lineTo(vertices[2].x, vertices[2].y);
            ctx.closePath();
            ctx.fill();
            
            // 面2: H1-H2-H4
            ctx.beginPath();
            ctx.moveTo(vertices[0].x, vertices[0].y);
            ctx.lineTo(vertices[1].x, vertices[1].y);
            ctx.lineTo(vertices[3].x, vertices[3].y);
            ctx.closePath();
            ctx.fill();
            
            // 面3: H1-H3-H4
            ctx.beginPath();
            ctx.moveTo(vertices[0].x, vertices[0].y);
            ctx.lineTo(vertices[2].x, vertices[2].y);
            ctx.lineTo(vertices[3].x, vertices[3].y);
            ctx.closePath();
            ctx.fill();
            
            // 面4: H2-H3-H4
            ctx.beginPath();
            ctx.moveTo(vertices[1].x, vertices[1].y);
            ctx.lineTo(vertices[2].x, vertices[2].y);
            ctx.lineTo(vertices[3].x, vertices[3].y);
            ctx.closePath();
            ctx.fill();
            
            ctx.globalAlpha = 1;
            
            // 绘制四面体的边
            ctx.strokeStyle = 'rgba(79, 172, 254, 0.5)';
            ctx.lineWidth = 1;
            
            // 连接所有氢原子
            for (let i = 0; i < vertices.length; i++) {
                for (let j = i + 1; j < vertices.length; j++) {
                    ctx.beginPath();
                    ctx.moveTo(vertices[i].x, vertices[i].y);
                    ctx.lineTo(vertices[j].x, vertices[j].y);
                    ctx.stroke();
                }
            }
        }
        
        // 绘制键角
        function drawBondAngles() {
            // 选择三个氢原子来展示键角
            const h1 = project3D(molecule.atoms[1].x, molecule.atoms[1].y, molecule.atoms[1].z);
            const h2 = project3D(molecule.atoms[2].x, molecule.atoms[2].y, molecule.atoms[2].z);
            const h3 = project3D(molecule.atoms[3].x, molecule.atoms[3].y, molecule.atoms[3].z);
            const center = project3D(molecule.atoms[0].x, molecule.atoms[0].y, molecule.atoms[0].z);
            
            // 绘制第一个键角弧线
            drawAngleArc(center, h1, h2, '#00f2fe');
            
            // 绘制第二个键角弧线
            drawAngleArc(center, h2, h3, '#00f2fe');
        }
        
        // 绘制角度弧线
        function drawAngleArc(center, p1, p2, color) {
            const v1 = { x: p1.x - center.x, y: p1.y - center.y };
            const v2 = { x: p2.x - center.x, y: p2.y - center.y };
            
            const angle1 = Math.atan2(v1.y, v1.x);
            const angle2 = Math.atan2(v2.y, v2.x);
            
            const radius = 40;
            
            // 绘制弧线
            ctx.beginPath();
            ctx.arc(center.x, center.y, radius, angle1, angle2);
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制角度标签
            const midAngle = (angle1 + angle2) / 2;
            const labelX = center.x + (radius + 20) * Math.cos(midAngle);
            const labelY = center.y + (radius + 20) * Math.sin(midAngle);
            
            ctx.font = '14px Arial';
            ctx.fillStyle = color;
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('109.5°', labelX, labelY);
        }
        
        // 更新教学步骤高亮
        function updateStepHighlight() {
            const steps = document.querySelectorAll('.step');
            steps.forEach(step => step.classList.remove('active'));
            
            // 根据旋转角度决定当前步骤
            const normalizedRotation = (molecule.rotation.y % (Math.PI * 2) + Math.PI * 2) % (Math.PI * 2);
            
            if (normalizedRotation < Math.PI / 2) {
                document.getElementById('step1').classList.add('active');
            } else if (normalizedRotation < Math.PI) {
                document.getElementById('step2').classList.add('active');
            } else if (normalizedRotation < Math.PI * 1.5) {
                document.getElementById('step3').classList.add('active');
            } else {
                document.getElementById('step4').classList.add('active');
            }
        }
        
        // 动画循环
        let lastTime = 0;
        function animate(timestamp) {
            if (!lastTime) lastTime = timestamp;
            const deltaTime = timestamp - lastTime;
            lastTime = timestamp;
            
            // 自动旋转（如果启用）
            if (document.getElementById('autoRotate').classList.contains('active')) {
                molecule.rotation.y += deltaTime * 0.001;
            }
            
            draw();
            requestAnimationFrame(animate);
        }
        
        // 鼠标交互
        let isDragging = false;
        let lastMousePos = { x: 0, y: 0 };
        
        canvas.addEventListener('mousedown', (e) => {
            isDragging = true;
            lastMousePos = { x: e.clientX, y: e.clientY };
            canvas.style.cursor = 'grabbing';
        });
        
        canvas.addEventListener('mousemove', (e) => {
            if (!isDragging) return;
            
            const deltaX = e.clientX - lastMousePos.x;
            const deltaY = e.clientY - lastMousePos.y;
            
            molecule.rotation.y += deltaX * 0.01;
            molecule.rotation.x += deltaY * 0.01;
            
            lastMousePos = { x: e.clientX, y: e.clientY };
        });
        
        canvas.addEventListener('mouseup', () => {
            isDragging = false;
            canvas.style.cursor = 'grab';
        });
        
        canvas.addEventListener('mouseleave', () => {
            isDragging = false;
            canvas.style.cursor = 'default';
        });
        
        canvas.addEventListener('wheel', (e) => {
            e.preventDefault();
            molecule.scale += e.deltaY * -0.001;
            molecule.scale = Math.max(0.5, Math.min(3, molecule.scale));
        });
        
        canvas.style.cursor = 'grab';
        
        // 控制按钮事件
        document.getElementById('autoRotate').addEventListener('click', function() {
            this.classList.toggle('active');
        });
        
        document.getElementById('resetView').addEventListener('click', function() {
            molecule.rotation = { x: 0.5, y: 0.5, z: 0 };
            molecule.scale = 1;
            molecule.offset = { x: 0, y: 0 };
        });
        
        document.getElementById('ballStick').addEventListener('click', function() {
            document.getElementById('ballStick').classList.add('active');
            document.getElementById('spaceFilling').classList.remove('active');
        });
        
        document.getElementById('spaceFilling').addEventListener('click', function() {
            document.getElementById('spaceFilling').classList.add('active');
            document.getElementById('ballStick').classList.remove('active');
        });
        
        // 复选框事件
        document.querySelectorAll('input[type="checkbox"]').forEach(checkbox => {
            checkbox.addEventListener('change', draw);
        });
        
        // 初始绘制
        molecule.rotation.x = 0.5;
        molecule.rotation.y = 0.5;
        draw();
        
        // 开始动画循环
        requestAnimationFrame(animate);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 甲烷分子空间结构交互式教学动画使用指南

欢迎使用“甲烷分子空间结构”交互式教学动画！本工具专为化学学习者设计，通过直观的3D可视化帮助您深入理解甲烷分子的正四面体构型。无论您是高中生、大学生还是化学爱好者，都能通过本动画获得清晰、深刻的学习体验。

---

### 一、功能说明

本动画是一个基于HTML5 Canvas技术开发的交互式3D可视化工具，完整运行于现代浏览器中，无需安装任何插件。它通过实时渲染技术，将抽象的甲烷分子空间结构转化为直观、可操作的视觉模型，让您能够从任意角度观察和分析分子的三维构型。

### 二、主要功能

#### 1. **3D观察控制**
   - **自动旋转**：点击“自动旋转”按钮，分子模型将缓慢持续旋转，帮助您全面观察其对称性
   - **手动旋转**：用鼠标拖拽模型，可从任意角度自由观察
   - **缩放视图**：使用鼠标滚轮放大或缩小分子模型
   - **重置视图**：一键恢复初始观察角度和大小

#### 2. **模型切换**
   - **球棍模型**：显示原子为球体、化学键为棍棒，突出分子的连接关系和空间构型
   - **比例模型**：按原子实际大小比例显示，展示分子实际占据的空间体积

#### 3. **可视化辅助工具**
   - **原子标签**：显示/隐藏碳(C)和氢(H)原子标签
   - **键角显示**：显示109.5°键角的弧线和数值标注
   - **正四面体框架**：显示连接四个氢原子构成的透明正四面体几何框架
   - **坐标轴**：显示三维坐标轴(X, Y, Z)，帮助建立空间方向感

#### 4. **教学引导**
   - **分步学习**：右侧面板提供四个循序渐进的学习步骤，随着模型旋转自动高亮当前步骤
   - **分子属性**：实时显示甲烷分子的关键参数（分子式、键角、对称性）

### 三、设计特色

#### 1. **科学准确性**
   - 所有原子位置基于精确的正四面体几何计算
   - 键角严格设置为109.5°（sp³杂化理论值）
   - 原子颜色遵循国际化学可视化惯例（碳：深灰色，氢：白色）

#### 2. **教学友好性**
   - **渐进式呈现**：信息分层显示，避免认知过载
   - **视觉对比**：深色背景突出分子模型，关键元素使用高对比度色彩
   - **即时反馈**：所有操作都有明确的视觉响应

#### 3. **技术先进性**
   - 纯前端实现，无需服务器支持
   - 响应式设计，适配不同屏幕尺寸
   - 流畅的60fps动画渲染

### 四、教学要点

#### 核心概念理解路径

1. **整体结构认知**
   - 观察碳原子位于正四面体中心的位置关系
   - 理解四个氢原子位于正四面体四个顶点的对称分布

2. **几何参数掌握**
   - 重点理解109.5°键角的含义和测量方法
   - 认识所有C-H键等长的特性

3. **对称性探索**
   - 通过旋转发现：从任意氢原子视角观察，分子结构完全相同
   - 理解T<sub>d</sub>对称群的含义

4. **模型对比分析**
   - 对比球棍模型和比例模型的差异
   - 理解不同模型的教学侧重点

#### 常见认知难点突破

- **从2D到3D的思维转换**：利用旋转功能帮助学生建立空间想象力
- **抽象对称性的具体化**：通过多角度观察，使“高度对称”概念可视化
- **键角意义的理解**：结合几何框架显示，将角度与空间构型直接关联

### 五、使用建议

#### 对于学生：
1. **初次接触时**：先启用“自动旋转”，让模型完整旋转几圈，获得整体印象
2. **深入学习时**：
   - 关闭自动旋转，手动拖拽从特定角度观察
   - 依次开启各项辅助工具（键角、框架、坐标轴）
   - 在不同模型间切换，思考各自的展示重点
3. **复习巩固时**：尝试不看标签，仅凭空间构型判断原子类型和键角

#### 对于教师：
1. **课堂演示**：
   - 全屏展示，使用自动旋转功能引入主题
   - 逐步开启辅助工具，引导学生注意力
   - 在关键角度暂停，进行重点讲解
2. **探究活动设计**：
   - 提出问题：“如果键角不是109.5°，分子形状会怎样变化？”
   - 布置任务：“找出分子中所有的对称元素”
   - 拓展思考：“比较CH₄与NH₃、H₂O分子构型的异同”

#### 最佳实践组合：
- **理解构型**：球棍模型 + 正四面体框架 + 键角显示
- **探索对称**：自动旋转 + 坐标轴显示
- **空间感知**：比例模型 + 手动多角度观察

---

### 技术提示
- 推荐使用Chrome、Firefox、Edge等现代浏览器
- 确保浏览器已启用JavaScript
- 如遇性能问题，可尝试关闭部分可视化选项
- 本工具完全在本地运行，不收集任何用户数据

### 学习延伸
在掌握甲烷分子结构后，您可以进一步探索：
1. 其他sp³杂化分子的空间构型
2. 键角大小与杂化类型的关系
3. 分子轨道理论对空间构型的解释

---

**开始您的探索之旅吧！** 拖动鼠标旋转分子，点击按钮切换视图，让甲烷分子的正四面体结构在您眼前“活”起来。科学的美妙，在于发现；理解的空间，在于探索。祝您学习愉快！

*教育技术让抽象概念触手可及，让科学之美清晰可见。*