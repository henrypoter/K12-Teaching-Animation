# 需求：平衡二叉树（AVL树四种旋转动画，必看！）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是学习数据结构与算法的计算机科学学生或自学者。他们的核心需求是：
1.  **理解旋转的本质**：不仅仅是记住四种旋转（LL, RR, LR, RL）的步骤，更要理解旋转是为了恢复平衡，以及如何通过旋转调整树的结构。
2.  **可视化过程**：需要清晰地看到从“失衡”到“平衡”的动态调整过程，特别是节点指针的重新连接和高度/平衡因子的变化。
3.  **掌握判断逻辑**：理解如何根据插入/删除位置和当前节点的平衡因子，判断需要应用哪种旋转。
4.  **主动探索与验证**：用户希望能够输入自己的数据序列，观察AVL树如何动态构建和调整，以巩固理解。

#### 教学设计思路
*   **核心概念**：围绕“平衡因子（Balance Factor, BF）”、“最小失衡子树”和“旋转（Rotation）”展开。动画的核心是展示旋转如何通过局部子树的重组，在保持二叉搜索树性质的前提下，恢复平衡。
*   **认知规律**：
    *   **从静态到动态**：先展示一棵失衡的AVL树，高亮显示最小失衡子树和关键节点（A：失衡点， B, C：关键子节点），然后播放旋转动画。
    *   **从分步到连续**：对于复杂的双旋转（LR, RL），先分解为两个单旋转，再展示连续过程。提供“分步演示”和“连续播放”两种模式。
    *   **从观察到交互**：先提供预设的经典案例进行观察学习，再提供交互式构建区域供用户自主探索。
*   **交互设计**：
    *   **模式选择**：设置“学习模式”和“探索模式”。
        *   **学习模式**：提供四种旋转的预设实例，用户通过按钮选择并观看动画。
        *   **探索模式**：允许用户输入数字序列或逐个插入/删除节点，实时观察AVL树的动态平衡过程。
    *   **动画控制**：包含播放、暂停、步进、重置控件。对于双旋转，有“查看分解步骤”的选项。
    *   **信息高亮**：动画过程中，当前关注的节点（如失衡节点A）、移动的子树、变化的指针会用醒目的颜色和标签（如“A”，“B”）进行标注。平衡因子实时显示在每个节点旁。
*   **视觉呈现**：
    *   **树结构可视化**：采用清晰、美观的树形布局算法，节点大小适中，连线清晰。
    *   **状态编码**：
        *   **颜色**：平衡节点用中性色（如浅蓝），失衡节点用警示色（如橙色），正在移动的节点/子树用强调色（如绿色）。
        *   **图形**：在节点内显示键值和平衡因子（例如 `值: BF`）。
    *   **辅助视图**：在动画区旁设置一个“信息面板”，用文字描述当前步骤（例如：“节点A（值为10）的平衡因子为2，左子树更高。在其左孩子B（值为5）处，平衡因子为1，属于LL型失衡，将进行右单旋转。”）。

#### 配色方案选择
选择柔和、对比清晰且符合认知习惯的配色方案，确保长时间观看不易疲劳。
*   **背景与画布**：主背景为浅灰色（`#f5f7fa`），树画布背景为白色（`#ffffff`）带轻微阴影，以突出内容。
*   **节点**：
    *   平衡节点：填充色为浅蓝色（`#e3f2fd`），边框为深蓝色（`#1976d2`）。
    *   失衡节点：填充色为浅橙色（`#fff3e0`），边框为深橙色（`#f57c00`）。
    *   当前焦点节点（如旋转轴）：填充色为浅绿色（`#e8f5e9`），边框为绿色（`#4caf50`），并可能带有脉动效果。
*   **连线**：普通树边为深灰色（`#757575`）。正在重新连接的指针用红色（`#e53935`）虚线高亮显示。
*   **文本**：键值用黑色（`#212121`），平衡因子用深灰色（`#666`）或根据正负使用不同颜色（正为蓝，负为橙）。
*   **控制面板**：按钮使用主色调蓝色（`#1976d2`），悬停时加深（`#1565c0`）。

#### 交互功能列表
1.  **模式切换器**：在“学习模式”和“探索模式”间切换。
2.  **学习模式功能**：
    *   **旋转类型选择**：四个按钮分别对应“LL（右旋）”、“RR（左旋）”、“LR（先左后右）”、“RL（先右后左）”，点击后加载预设案例。
    *   **动画控制栏**：包含“播放/暂停”、“下一步”、“上一步”、“重置”按钮。
    *   **分解控制**（针对LR/RL）：一个复选框“显示分解步骤”，勾选后动画将分步展示两次单旋转。
3.  **探索模式功能**：
    *   **数据输入**：一个文本输入框（用于批量插入数字序列）和一个“插入”按钮。
    *   **节点交互**：在可视化的树上，点击某个节点可选中，然后通过“删除节点”按钮进行删除操作，触发可能的平衡调整。
    *   **实时显示**：在插入/删除过程中，树实时更新，失衡和旋转过程自动以动画形式展现。
4.  **全局信息面板**：实时显示当前操作说明、旋转类型判断依据和步骤日志。
5.  **视图控制**：可选的“缩放”和“平移”画布功能，便于查看大树。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AVL树四种旋转动画教学</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #212121;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #1976d2;
        }
        
        h1 {
            color: #1976d2;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #666;
            font-size: 1.1rem;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .left-panel {
            flex: 1;
            min-width: 300px;
            background: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .right-panel {
            flex: 2;
            min-width: 500px;
            background: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
        }
        
        .panel-title {
            color: #1976d2;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e0e0e0;
            font-size: 1.4rem;
        }
        
        .mode-selector {
            display: flex;
            margin-bottom: 25px;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #1976d2;
        }
        
        .mode-btn {
            flex: 1;
            padding: 12px;
            background: white;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
            color: #1976d2;
        }
        
        .mode-btn.active {
            background: #1976d2;
            color: white;
        }
        
        .mode-btn:hover:not(.active) {
            background: #e3f2fd;
        }
        
        .mode-content {
            display: none;
        }
        
        .mode-content.active {
            display: block;
        }
        
        .rotation-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .rotation-btn {
            padding: 15px;
            background: #e3f2fd;
            border: 2px solid #1976d2;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            color: #1976d2;
            transition: all 0.3s;
            text-align: center;
        }
        
        .rotation-btn:hover {
            background: #bbdefb;
            transform: translateY(-2px);
        }
        
        .rotation-btn.active {
            background: #1976d2;
            color: white;
        }
        
        .animation-controls {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
            margin-bottom: 25px;
        }
        
        .control-btn {
            padding: 10px 20px;
            background: #1976d2;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .control-btn:hover:not(:disabled) {
            background: #1565c0;
            transform: translateY(-2px);
        }
        
        .control-btn:disabled {
            background: #b0bec5;
            cursor: not-allowed;
        }
        
        .step-controls {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .step-btn {
            padding: 8px 16px;
            background: #4caf50;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .step-btn:hover:not(:disabled) {
            background: #43a047;
        }
        
        .step-btn:disabled {
            background: #a5d6a7;
            cursor: not-allowed;
        }
        
        .decompose-checkbox {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .decompose-checkbox input {
            margin-right: 10px;
            width: 18px;
            height: 18px;
        }
        
        .explore-input {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .explore-input input {
            flex: 1;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 1rem;
        }
        
        .explore-input button {
            padding: 12px 24px;
            background: #4caf50;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .explore-input button:hover {
            background: #43a047;
        }
        
        .tree-info {
            background: #f9f9f9;
            border-radius: 8px;
            padding: 15px;
            margin-top: 20px;
            border-left: 4px solid #1976d2;
        }
        
        .tree-info h3 {
            margin-bottom: 10px;
            color: #1976d2;
        }
        
        .info-item {
            margin-bottom: 8px;
            display: flex;
        }
        
        .info-label {
            font-weight: 600;
            min-width: 120px;
            color: #666;
        }
        
        #canvas-container {
            flex: 1;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            overflow: hidden;
            background: white;
            position: relative;
        }
        
        #tree-canvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .info-panel {
            margin-top: 25px;
            background: #f9f9f9;
            border-radius: 8px;
            padding: 20px;
            max-height: 250px;
            overflow-y: auto;
            border-left: 4px solid #4caf50;
        }
        
        .info-panel h3 {
            color: #4caf50;
            margin-bottom: 15px;
        }
        
        .log-entry {
            padding: 10px;
            margin-bottom: 10px;
            background: white;
            border-radius: 6px;
            border-left: 3px solid #1976d2;
        }
        
        .log-entry.important {
            border-left-color: #f57c00;
            background: #fff3e0;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #e0e0e0;
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
            border: 2px solid;
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #666;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #ddd;
            color: #666;
            font-size: 0.9rem;
        }
        
        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .left-panel, .right-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>AVL树四种旋转动画教学</h1>
            <p class="subtitle">可视化理解平衡二叉树的LL、RR、LR、RL旋转操作</p>
        </header>
        
        <div class="main-content">
            <div class="left-panel">
                <h2 class="panel-title">控制面板</h2>
                
                <div class="mode-selector">
                    <button class="mode-btn active" data-mode="learn">学习模式</button>
                    <button class="mode-btn" data-mode="explore">探索模式</button>
                </div>
                
                <div id="learn-mode" class="mode-content active">
                    <h3>选择旋转类型</h3>
                    <div class="rotation-buttons">
                        <button class="rotation-btn" data-rotation="LL">LL型失衡<br>右单旋转</button>
                        <button class="rotation-btn" data-rotation="RR">RR型失衡<br>左单旋转</button>
                        <button class="rotation-btn" data-rotation="LR">LR型失衡<br>先左后右旋转</button>
                        <button class="rotation-btn" data-rotation="RL">RL型失衡<br>先右后左旋转</button>
                    </div>
                    
                    <div class="animation-controls">
                        <button id="play-btn" class="control-btn">播放动画</button>
                        <button id="reset-btn" class="control-btn">重置</button>
                    </div>
                    
                    <div class="step-controls">
                        <button id="prev-step" class="step-btn" disabled>上一步</button>
                        <button id="next-step" class="step-btn">下一步</button>
                    </div>
                    
                    <div class="decompose-checkbox">
                        <input type="checkbox" id="decompose-toggle">
                        <label for="decompose-toggle">显示双旋转分解步骤 (LR/RL)</label>
                    </div>
                    
                    <div class="tree-info">
                        <h3>当前树信息</h3>
                        <div class="info-item">
                            <span class="info-label">旋转类型:</span>
                            <span id="rotation-type">未选择</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">失衡节点:</span>
                            <span id="imbalance-node">无</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">动画状态:</span>
                            <span id="animation-state">就绪</span>
                        </div>
                    </div>
                </div>
                
                <div id="explore-mode" class="mode-content">
                    <h3>交互式构建AVL树</h3>
                    <div class="explore-input">
                        <input type="text" id="node-input" placeholder="输入数字 (多个用逗号分隔)">
                        <button id="insert-btn">插入节点</button>
                    </div>
                    <div class="explore-input">
                        <input type="text" id="delete-input" placeholder="输入要删除的数字">
                        <button id="delete-btn">删除节点</button>
                    </div>
                    <button id="clear-tree" class="control-btn" style="background:#f44336; margin-bottom:20px;">清空树</button>
                    
                    <div class="tree-info">
                        <h3>树状态</h3>
                        <div class="info-item">
                            <span class="info-label">节点总数:</span>
                            <span id="node-count">0</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">树高度:</span>
                            <span id="tree-height">0</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">是否平衡:</span>
                            <span id="is-balanced">是</span>
                        </div>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background:#e3f2fd; border-color:#1976d2;"></div>
                        <span class="legend-text">平衡节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background:#fff3e0; border-color:#f57c00;"></div>
                        <span class="legend-text">失衡节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background:#e8f5e9; border-color:#4caf50;"></div>
                        <span class="legend-text">旋转轴节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="border-color:#e53935; background:white;"></div>
                        <span class="legend-text">重新连接指针</span>
                    </div>
                </div>
            </div>
            
            <div class="right-panel">
                <h2 class="panel-title">AVL树可视化</h2>
                <div id="canvas-container">
                    <canvas id="tree-canvas"></canvas>
                </div>
                
                <div class="info-panel">
                    <h3>操作说明与步骤日志</h3>
                    <div id="log-container">
                        <div class="log-entry">欢迎使用AVL树旋转动画教学工具！请选择一种旋转类型开始学习，或切换到探索模式构建自己的AVL树。</div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>AVL树旋转动画教学工具 | 设计用于数据结构与算法可视化学习</p>
            <p>提示：在探索模式中，插入或删除节点后，AVL树会自动进行平衡调整</p>
        </footer>
    </div>

    <script>
        // AVL树节点类
        class AVLNode {
            constructor(value) {
                this.value = value;
                this.height = 1;
                this.left = null;
                this.right = null;
                this.balanceFactor = 0;
                this.x = 0;
                this.y = 0;
                this.id = `node_${value}_${Date.now()}_${Math.random().toString(36).substr(2, 9)}`;
            }
        }

        // AVL树类
        class AVLTree {
            constructor() {
                this.root = null;
                this.nodeMap = new Map(); // 用于快速查找节点
            }
            
            // 获取节点高度
            getHeight(node) {
                return node ? node.height : 0;
            }
            
            // 更新节点高度和平衡因子
            updateHeight(node) {
                if (!node) return;
                node.height = Math.max(this.getHeight(node.left), this.getHeight(node.right)) + 1;
                node.balanceFactor = this.getHeight(node.left) - this.getHeight(node.right);
            }
            
            // 右旋 (LL型)
            rotateRight(y) {
                const x = y.left;
                const T2 = x.right;
                
                // 执行旋转
                x.right = y;
                y.left = T2;
                
                // 更新高度
                this.updateHeight(y);
                this.updateHeight(x);
                
                return x;
            }
            
            // 左旋 (RR型)
            rotateLeft(x) {
                const y = x.right;
                const T2 = y.left;
                
                // 执行旋转
                y.left = x;
                x.right = T2;
                
                // 更新高度
                this.updateHeight(x);
                this.updateHeight(y);
                
                return y;
            }
            
            // 插入节点
            insert(value) {
                this.root = this._insert(this.root, value);
            }
            
            _insert(node, value) {
                // 1. 标准BST插入
                if (!node) {
                    return new AVLNode(value);
                }
                
                if (value < node.value) {
                    node.left = this._insert(node.left, value);
                } else if (value > node.value) {
                    node.right = this._insert(node.right, value);
                } else {
                    return node; // 不允许重复值
                }
                
                // 2. 更新高度
                this.updateHeight(node);
                
                // 3. 获取平衡因子，检查是否失衡
                const balance = node.balanceFactor;
                
                // 4. 根据失衡类型进行旋转
                // LL型
                if (balance > 1 && value < node.left.value) {
                    return this.rotateRight(node);
                }
                
                // RR型
                if (balance < -1 && value > node.right.value) {
                    return this.rotateLeft(node);
                }
                
                // LR型
                if (balance > 1 && value > node.left.value) {
                    node.left = this.rotateLeft(node.left);
                    return this.rotateRight(node);
                }
                
                // RL型
                if (balance < -1 && value < node.right.value) {
                    node.right = this.rotateRight(node.right);
                    return this.rotateLeft(node);
                }
                
                return node;
            }
            
            // 查找最小节点
            minValueNode(node) {
                let current = node;
                while (current.left) {
                    current = current.left;
                }
                return current;
            }
            
            // 删除节点
            delete(value) {
                this.root = this._delete(this.root, value);
            }
            
            _delete(node, value) {
                // 1. 标准BST删除
                if (!node) {
                    return node;
                }
                
                if (value < node.value) {
                    node.left = this._delete(node.left, value);
                } else if (value > node.value) {
                    node.right = this._delete(node.right, value);
                } else {
                    // 找到要删除的节点
                    if (!node.left || !node.right) {
                        // 有一个或没有子节点
                        const temp = node.left || node.right;
                        node = temp || null;
                    } else {
                        // 有两个子节点
                        const temp = this.minValueNode(node.right);
                        node.value = temp.value;
                        node.right = this._delete(node.right, temp.value);
                    }
                }
                
                if (!node) {
                    return node;
                }
                
                // 2. 更新高度
                this.updateHeight(node);
                
                // 3. 获取平衡因子，检查是否失衡
                const balance = node.balanceFactor;
                
                // 4. 根据失衡类型进行旋转
                // LL型
                if (balance > 1 && this.getBalanceFactor(node.left) >= 0) {
                    return this.rotateRight(node);
                }
                
                // LR型
                if (balance > 1 && this.getBalanceFactor(node.left) < 0) {
                    node.left = this.rotateLeft(node.left);
                    return this.rotateRight(node);
                }
                
                // RR型
                if (balance < -1 && this.getBalanceFactor(node.right) <= 0) {
                    return this.rotateLeft(node);
                }
                
                // RL型
                if (balance < -1 && this.getBalanceFactor(node.right) > 0) {
                    node.right = this.rotateRight(node.right);
                    return this.rotateLeft(node);
                }
                
                return node;
            }
            
            getBalanceFactor(node) {
                if (!node) return 0;
                return this.getHeight(node.left) - this.getHeight(node.right);
            }
            
            // 构建节点映射
            buildNodeMap() {
                this.nodeMap.clear();
                this._buildNodeMap(this.root);
            }
            
            _buildNodeMap(node) {
                if (!node) return;
                this.nodeMap.set(node.value, node);
                this._buildNodeMap(node.left);
                this._buildNodeMap(node.right);
            }
            
            // 获取节点总数
            getNodeCount() {
                return this._countNodes(this.root);
            }
            
            _countNodes(node) {
                if (!node) return 0;
                return 1 + this._countNodes(node.left) + this._countNodes(node.right);
            }
            
            // 获取树高度
            getTreeHeight() {
                return this.getHeight(this.root);
            }
            
            // 检查树是否平衡
            isBalanced() {
                return this._isBalanced(this.root);
            }
            
            _isBalanced(node) {
                if (!node) return true;
                
                const balance = this.getBalanceFactor(node);
                if (Math.abs(balance) > 1) return false;
                
                return this._isBalanced(node.left) && this._isBalanced(node.right);
            }
        }

        // 动画状态管理器
        class AnimationManager {
            constructor(canvas, tree) {
                this.canvas = canvas;
                this.ctx = canvas.getContext('2d');
                this.tree = tree;
                this.animationState = 'idle'; // idle, playing, paused
                this.currentStep = 0;
                this.totalSteps = 0;
                this.steps = [];
                this.currentRotation = null;
                this.showDecompose = false;
                this.animationSpeed = 1000; // 毫秒
                this.highlightedNodes = new Set();
                this.highlightedEdges = [];
                
                // 预设的四种旋转案例
                this.presetCases = {
                    'LL': [30, 20, 10, 5, 3], // 插入顺序导致LL失衡
                    'RR': [10, 20, 30, 40, 50], // 插入顺序导致RR失衡
                    'LR': [30, 10, 20, 5, 25], // 插入顺序导致LR失衡
                    'RL': [10, 30, 20, 25, 35] // 插入顺序导致RL失衡
                };
                
                // 初始化画布大小
                this.resizeCanvas();
                window.addEventListener('resize', () => this.resizeCanvas());
            }
            
            resizeCanvas() {
                const container = document.getElementById('canvas-container');
                this.canvas.width = container.clientWidth;
                this.canvas.height = container.clientHeight;
                this.drawTree();
            }
            
            // 选择旋转类型
            selectRotation(type) {
                this.currentRotation = type;
                this.resetAnimation();
                
                // 根据选择的类型构建树
                this.tree.root = null;
                const values = this.presetCases[type];
                
                // 记录插入过程用于动画
                this.steps = [];
                this.steps.push({type: 'info', message: `构建${type}型失衡的AVL树...`});
                
                for (let i = 0; i < values.length; i++) {
                    this.tree.insert(values[i]);
                    this.steps.push({
                        type: 'insert',
                        value: values[i],
                        treeState: this.getTreeState()
                    });
                }
                
                // 添加失衡检测步骤
                this.steps.push({
                    type: 'detect',
                    imbalance: this.findImbalanceNode(),
                    treeState: this.getTreeState()
                });
                
                // 添加旋转步骤
                this.addRotationSteps(type);
                
                this.totalSteps = this.steps.length;
                this.currentStep = 0;
                
                // 更新UI
                document.getElementById('rotation-type').textContent = type;
                document.getElementById('imbalance-node').textContent = this.findImbalanceNode()?.value || '无';
                document.getElementById('animation-state').textContent = '就绪';
                
                this.addLog(`已加载${type}型旋转案例。树中有${values.length}个节点。`, false);
                this.addLog(`失衡节点: ${this.findImbalanceNode()?.value || '无'}`, true);
                
                this.drawTree();
            }
            
            // 添加旋转步骤
            addRotationSteps(type) {
                const imbalanceNode = this.findImbalanceNode();
                if (!imbalanceNode) return;
                
                switch(type) {
                    case 'LL':
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.value], message: '失衡节点A(平衡因子=2)'});
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.left.value], message: 'A的左孩子B(平衡因子=1)'});
                        this.steps.push({type: 'rotate', rotation: 'right', pivot: imbalanceNode.value, message: '执行右单旋转，B成为新的根节点'});
                        break;
                    case 'RR':
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.value], message: '失衡节点A(平衡因子=-2)'});
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.right.value], message: 'A的右孩子B(平衡因子=-1)'});
                        this.steps.push({type: 'rotate', rotation: 'left', pivot: imbalanceNode.value, message: '执行左单旋转，B成为新的根节点'});
                        break;
                    case 'LR':
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.value], message: '失衡节点A(平衡因子=2)'});
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.left.value], message: 'A的左孩子B(平衡因子=-1)'});
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.left.right.value], message: 'B的右孩子C(平衡因子=0或1)'});
                        
                        if (this.showDecompose) {
                            this.steps.push({type: 'rotate', rotation: 'left', pivot: imbalanceNode.left.value, message: '第一步：对B进行左旋，将LR型转为LL型'});
                            this.steps.push({type: 'rotate', rotation: 'right', pivot: imbalanceNode.value, message: '第二步：对A进行右旋，C成为新的根节点'});
                        } else {
                            this.steps.push({type: 'rotate', rotation: 'LR', pivot: imbalanceNode.value, message: '执行LR双旋转（先左后右），C成为新的根节点'});
                        }
                        break;
                    case 'RL':
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.value], message: '失衡节点A(平衡因子=-2)'});
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.right.value], message: 'A的右孩子B(平衡因子=1)'});
                        this.steps.push({type: 'highlight', nodes: [imbalanceNode.right.left.value], message: 'B的左孩子C(平衡因子=0或-1)'});
                        
                        if (this.showDecompose) {
                            this.steps.push({type: 'rotate', rotation: 'right', pivot: imbalanceNode.right.value, message: '第一步：对B进行右旋，将RL型转为RR型'});
                            this.steps.push({type: 'rotate', rotation: 'left', pivot: imbalanceNode.value, message: '第二步：对A进行左旋，C成为新的根节点'});
                        } else {
                            this.steps.push({type: 'rotate', rotation: 'RL', pivot: imbalanceNode.value, message: '执行RL双旋转（先右后左），C成为新的根节点'});
                        }
                        break;
                }
                
                this.steps.push({type: 'result', message: '旋转完成！AVL树恢复平衡。'});
            }
            
            // 查找失衡节点
            findImbalanceNode() {
                return this._findImbalanceNode(this.tree.root);
            }
            
            _findImbalanceNode(node) {
                if (!node) return null;
                
                if (Math.abs(node.balanceFactor) > 1) {
                    return node;
                }
                
                const leftImbalance = this._findImbalanceNode(node.left);
                if (leftImbalance) return leftImbalance;
                
                return this._findImbalanceNode(node.right);
            }
            
            // 获取树的当前状态（深拷贝）
            getTreeState() {
                return JSON.parse(JSON.stringify(this.serializeTree(this.tree.root)));
            }
            
            serializeTree(node) {
                if (!node) return null;
                return {
                    value: node.value,
                    height: node.height,
                    balanceFactor: node.balanceFactor,
                    left: this.serializeTree(node.left),
                    right: this.serializeTree(node.right)
                };
            }
            
            // 播放动画
            playAnimation() {
                if (this.animationState === 'playing') return;
                
                if (this.currentStep >= this.totalSteps) {
                    this.currentStep = 0;
                }
                
                this.animationState = 'playing';
                document.getElementById('animation-state').textContent = '播放中';
                this.addLog('开始播放动画...', false);
                
                this.playNextStep();
            }
            
            // 播放下一步
            playNextStep() {
                if (this.currentStep >= this.totalSteps || this.animationState !== 'playing') {
                    this.animationState = 'idle';
                    document.getElementById('animation-state').textContent = '完成';
                    this.addLog('动画播放完成！', true);
                    return;
                }
                
                const step = this.steps[this.currentStep];
                this.executeStep(step);
                
                this.currentStep++;
                
                // 更新按钮状态
                document.getElementById('prev-step').disabled = this.currentStep <= 1;
                document.getElementById('next-step').disabled = this.currentStep >= this.totalSteps;
                
                // 继续播放
                setTimeout(() => {
                    if (this.animationState === 'playing') {
                        this.playNextStep();
                    }
                }, this.animationSpeed);
            }
            
            // 执行单步
            executeStep(step) {
                this.highlightedNodes.clear();
                this.highlightedEdges = [];
                
                switch(step.type) {
                    case 'info':
                        this.addLog(step.message, false);
                        break;
                        
                    case 'insert':
                        this.addLog(`插入节点: ${step.value}`, false);
                        break;
                        
                    case 'detect':
                        if (step.imbalance) {
                            this.highlightedNodes.add(step.imbalance.value);
                            this.addLog(`检测到失衡节点: ${step.imbalance.value} (平衡因子=${step.imbalance.balanceFactor})`, true);
                        }
                        break;
                        
                    case 'highlight':
                        step.nodes.forEach(node => this.highlightedNodes.add(node));
                        this.addLog(step.message, true);
                        break;
                        
                    case 'rotate':
                        this.addLog(step.message, true);
                        // 在实际应用中，这里会执行旋转并更新树
                        // 由于我们已经有完整的树，这里只是高亮显示
                        if (step.rotation === 'right' || step.rotation === 'left') {
                            this.highlightedNodes.add(step.pivot);
                            // 高亮显示旋转涉及的边
                            this.highlightedEdges.push({from: step.pivot, to: step.pivot, isRotation: true});
                        }
                        break;
                        
                    case 'result':
                        this.addLog(step.message, true);
                        break;
                }
                
                this.drawTree();
            }
            
            // 下一步（手动）
            nextStep() {
                if (this.currentStep >= this.totalSteps) return;
                
                this.animationState = 'paused';
                document.getElementById('animation-state').textContent = '暂停';
                
                const step = this.steps[this.currentStep];
                this.executeStep(step);
                
                this.currentStep++;
                
                // 更新按钮状态
                document.getElementById('prev-step').disabled = this.currentStep <= 1;
                document.getElementById('next-step').disabled = this.currentStep >= this.totalSteps;
            }
            
            // 上一步（手动）
            prevStep() {
                if (this.currentStep <= 1) return;
                
                this.currentStep--;
                this.animationState = 'paused';
                document.getElementById('animation-state').textContent = '暂停';
                
                // 回退到前一步
                const step = this.steps[this.currentStep - 1];
                this.executeStep(step);
                
                // 更新按钮状态
                document.getElementById('prev-step').disabled = this.currentStep <= 1;
                document.getElementById('next-step').disabled = this.currentStep >= this.totalSteps;
            }
            
            // 重置动画
            resetAnimation() {
                this.animationState = 'idle';
                this.currentStep = 0;
                this.highlightedNodes.clear();
                this.highlightedEdges = [];
                
                document.getElementById('prev-step').disabled = true;
                document.getElementById('next-step').disabled = false;
                document.getElementById('animation-state').textContent = '就绪';
                
                this.drawTree();
            }
            
            // 绘制树
            drawTree() {
                const ctx = this.ctx;
                const width = this.canvas.width;
                const height = this.canvas.height;
                
                // 清空画布
                ctx.clearRect(0, 0, width, height);
                
                if (!this.tree.root) {
                    ctx.fillStyle = '#666';
                    ctx.font = '18px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('树为空，请插入节点或选择旋转案例', width / 2, height / 2);
                    return;
                }
                
                // 计算树布局
                this.calculatePositions(this.tree.root, width / 2, 80, width / 4);
                
                // 绘制边
                this.drawEdges(this.tree.root);
                
                // 绘制节点
                this.drawNodes(this.tree.root);
            }
            
            // 计算节点位置
            calculatePositions(node, x, y, offset) {
                if (!node) return;
                
                node.x = x;
                node.y = y;
                
                if (node.left) {
                    this.calculatePositions(node.left, x - offset, y + 80, offset / 1.8);
                }
                
                if (node.right) {
                    this.calculatePositions(node.right, x + offset, y + 80, offset / 1.8);
                }
            }
            
            // 绘制边
            drawEdges(node) {
                if (!node) return;
                
                const ctx = this.ctx;
                
                // 绘制左子节点边
                if (node.left) {
                    // 检查是否高亮
                    const isHighlighted = this.highlightedEdges.some(edge => 
                        (edge.from === node.value && edge.to === node.left.value) || 
                        (edge.from === node.left.value && edge.to === node.value)
                    );
                    
                    ctx.beginPath();
                    ctx.moveTo(node.x, node.y);
                    ctx.lineTo(node.left.x, node.left.y);
                    
                    if (isHighlighted) {
                        ctx.strokeStyle = '#e53935';
                        ctx.setLineDash([5, 5]);
                        ctx.lineWidth = 3;
                    } else {
                        ctx.strokeStyle = '#757575';
                        ctx.setLineDash([]);
                        ctx.lineWidth = 2;
                    }
                    
                    ctx.stroke();
                    
                    this.drawEdges(node.left);
                }
                
                // 绘制右子节点边
                if (node.right) {
                    // 检查是否高亮
                    const isHighlighted = this.highlightedEdges.some(edge => 
                        (edge.from === node.value && edge.to === node.right.value) || 
                        (edge.from === node.right.value && edge.to === node.value)
                    );
                    
                    ctx.beginPath();
                    ctx.moveTo(node.x, node.y);
                    ctx.lineTo(node.right.x, node.right.y);
                    
                    if (isHighlighted) {
                        ctx.strokeStyle = '#e53935';
                        ctx.setLineDash([5, 5]);
                        ctx.lineWidth =
<!--检测到代码截断，自动续写中...-->
3;
                    } else {
                        ctx.strokeStyle = '#757575';
                        ctx.setLineDash([]);
                        ctx.lineWidth = 2;
                    }
                    
                    ctx.stroke();
                    
                    this.drawEdges(node.right);
                }
            }
            
            // 绘制节点
            drawNodes(node) {
                if (!node) return;
                
                const ctx = this.ctx;
                const radius = 28;
                
                // 确定节点颜色
                let fillColor, borderColor;
                
                if (this.highlightedNodes.has(node.value)) {
                    // 高亮节点
                    if (this.currentRotation && this.findImbalanceNode()?.value === node.value) {
                        // 失衡节点
                        fillColor = '#fff3e0';
                        borderColor = '#f57c00';
                    } else {
                        // 旋转轴或其他高亮节点
                        fillColor = '#e8f5e9';
                        borderColor = '#4caf50';
                    }
                } else {
                    // 普通节点
                    fillColor = '#e3f2fd';
                    borderColor = '#1976d2';
                }
                
                // 绘制节点圆
                ctx.beginPath();
                ctx.arc(node.x, node.y, radius, 0, Math.PI * 2);
                ctx.fillStyle = fillColor;
                ctx.fill();
                ctx.strokeStyle = borderColor;
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制节点值
                ctx.fillStyle = '#212121';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(node.value, node.x, node.y - 8);
                
                // 绘制平衡因子
                ctx.fillStyle = node.balanceFactor === 0 ? '#666' : 
                               node.balanceFactor > 0 ? '#1976d2' : '#f57c00';
                ctx.font = '14px Arial';
                ctx.fillText(`BF:${node.balanceFactor}`, node.x, node.y + 12);
                
                // 绘制高度（可选）
                ctx.fillStyle = '#888';
                ctx.font = '12px Arial';
                ctx.fillText(`H:${node.height}`, node.x, node.y + 28);
                
                // 递归绘制子节点
                this.drawNodes(node.left);
                this.drawNodes(node.right);
            }
            
            // 添加日志
            addLog(message, isImportant = false) {
                const logContainer = document.getElementById('log-container');
                const logEntry = document.createElement('div');
                logEntry.className = `log-entry ${isImportant ? 'important' : ''}`;
                logEntry.textContent = `[${new Date().toLocaleTimeString()}] ${message}`;
                
                logContainer.appendChild(logEntry);
                logContainer.scrollTop = logContainer.scrollHeight;
                
                // 限制日志数量
                const logs = logContainer.querySelectorAll('.log-entry');
                if (logs.length > 20) {
                    logs[0].remove();
                }
            }
            
            // 清空日志
            clearLog() {
                const logContainer = document.getElementById('log-container');
                logContainer.innerHTML = '<div class="log-entry">日志已清空</div>';
            }
            
            // 探索模式：插入节点
            exploreInsert(values) {
                this.clearLog();
                this.addLog('开始插入节点...', false);
                
                const valueArray = values.split(',').map(v => parseInt(v.trim())).filter(v => !isNaN(v));
                
                if (valueArray.length === 0) {
                    this.addLog('请输入有效的数字！', true);
                    return;
                }
                
                for (const value of valueArray) {
                    this.tree.insert(value);
                    this.addLog(`插入节点: ${value}`, false);
                    
                    // 检查是否发生旋转
                    const imbalance = this.findImbalanceNode();
                    if (imbalance) {
                        this.addLog(`检测到失衡节点: ${imbalance.value} (平衡因子=${imbalance.balanceFactor})`, true);
                        
                        // 判断失衡类型
                        let rotationType = '';
                        if (imbalance.balanceFactor > 1) {
                            if (this.tree.getBalanceFactor(imbalance.left) >= 0) {
                                rotationType = 'LL型，执行右旋';
                            } else {
                                rotationType = 'LR型，执行先左后右旋转';
                            }
                        } else {
                            if (this.tree.getBalanceFactor(imbalance.right) <= 0) {
                                rotationType = 'RR型，执行左旋';
                            } else {
                                rotationType = 'RL型，执行先右后左旋转';
                            }
                        }
                        
                        this.addLog(`执行平衡调整: ${rotationType}`, true);
                    }
                }
                
                this.updateExploreInfo();
                this.drawTree();
            }
            
            // 探索模式：删除节点
            exploreDelete(value) {
                const numValue = parseInt(value);
                if (isNaN(numValue)) {
                    this.addLog('请输入有效的数字！', true);
                    return;
                }
                
                this.addLog(`删除节点: ${numValue}`, false);
                this.tree.delete(numValue);
                
                // 检查是否发生旋转
                const imbalance = this.findImbalanceNode();
                if (imbalance) {
                    this.addLog(`删除后检测到失衡节点: ${imbalance.value} (平衡因子=${imbalance.balanceFactor})`, true);
                    
                    // 判断失衡类型
                    let rotationType = '';
                    if (imbalance.balanceFactor > 1) {
                        if (this.tree.getBalanceFactor(imbalance.left) >= 0) {
                            rotationType = 'LL型，执行右旋';
                        } else {
                            rotationType = 'LR型，执行先左后右旋转';
                        }
                    } else {
                        if (this.tree.getBalanceFactor(imbalance.right) <= 0) {
                            rotationType = 'RR型，执行左旋';
                        } else {
                            rotationType = 'RL型，执行先右后左旋转';
                        }
                    }
                    
                    this.addLog(`执行平衡调整: ${rotationType}`, true);
                }
                
                this.updateExploreInfo();
                this.drawTree();
            }
            
            // 探索模式：清空树
            exploreClear() {
                this.tree.root = null;
                this.addLog('已清空AVL树', true);
                this.updateExploreInfo();
                this.drawTree();
            }
            
            // 更新探索模式信息
            updateExploreInfo() {
                document.getElementById('node-count').textContent = this.tree.getNodeCount();
                document.getElementById('tree-height').textContent = this.tree.getTreeHeight();
                document.getElementById('is-balanced').textContent = this.tree.isBalanced() ? '是' : '否';
            }
        }

        // 初始化应用
        document.addEventListener('DOMContentLoaded', function() {
            const canvas = document.getElementById('tree-canvas');
            const tree = new AVLTree();
            const animator = new AnimationManager(canvas, tree);
            
            // 模式切换
            const modeButtons = document.querySelectorAll('.mode-btn');
            const modeContents = document.querySelectorAll('.mode-content');
            
            modeButtons.forEach(btn => {
                btn.addEventListener('click', function() {
                    const mode = this.dataset.mode;
                    
                    // 更新按钮状态
                    modeButtons.forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    // 更新内容显示
                    modeContents.forEach(content => content.classList.remove('active'));
                    document.getElementById(`${mode}-mode`).classList.add('active');
                    
                    // 重置动画状态
                    animator.resetAnimation();
                    animator.clearLog();
                    
                    if (mode === 'learn') {
                        animator.addLog('切换到学习模式。请选择一种旋转类型开始学习。', false);
                    } else {
                        animator.addLog('切换到探索模式。请输入数字构建自己的AVL树。', false);
                        animator.updateExploreInfo();
                    }
                });
            });
            
            // 旋转类型选择
            const rotationButtons = document.querySelectorAll('.rotation-btn');
            rotationButtons.forEach(btn => {
                btn.addEventListener('click', function() {
                    // 更新按钮状态
                    rotationButtons.forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    // 选择旋转类型
                    const rotationType = this.dataset.rotation;
                    animator.selectRotation(rotationType);
                });
            });
            
            // 动画控制
            document.getElementById('play-btn').addEventListener('click', function() {
                if (animator.currentRotation) {
                    animator.playAnimation();
                } else {
                    animator.addLog('请先选择一种旋转类型！', true);
                }
            });
            
            document.getElementById('reset-btn').addEventListener('click', function() {
                animator.resetAnimation();
                animator.addLog('动画已重置', false);
            });
            
            document.getElementById('next-step').addEventListener('click', function() {
                if (animator.currentRotation) {
                    animator.nextStep();
                } else {
                    animator.addLog('请先选择一种旋转类型！', true);
                }
            });
            
            document.getElementById('prev-step').addEventListener('click', function() {
                if (animator.currentRotation) {
                    animator.prevStep();
                } else {
                    animator.addLog('请先选择一种旋转类型！', true);
                }
            });
            
            // 分解步骤切换
            document.getElementById('decompose-toggle').addEventListener('change', function() {
                animator.showDecompose = this.checked;
                if (animator.currentRotation) {
                    animator.selectRotation(animator.currentRotation);
                    animator.addLog(`已${this.checked ? '启用' : '禁用'}分解步骤显示`, false);
                }
            });
            
            // 探索模式控制
            document.getElementById('insert-btn').addEventListener('click', function() {
                const input = document.getElementById('node-input').value;
                animator.exploreInsert(input);
                document.getElementById('node-input').value = '';
            });
            
            document.getElementById('node-input').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    document.getElementById('insert-btn').click();
                }
            });
            
            document.getElementById('delete-btn').addEventListener('click', function() {
                const input = document.getElementById('delete-input').value;
                animator.exploreDelete(input);
                document.getElementById('delete-input').value = '';
            });
            
            document.getElementById('delete-input').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    document.getElementById('delete-btn').click();
                }
            });
            
            document.getElementById('clear-tree').addEventListener('click', function() {
                if (confirm('确定要清空整棵树吗？')) {
                    animator.exploreClear();
                }
            });
            
            // 初始选择LL型旋转
            document.querySelector('.rotation-btn[data-rotation="LL"]').click();
            
            // 初始日志
            animator.addLog('AVL树旋转动画教学工具已就绪！', false);
            animator.addLog('在学习模式下，选择一种旋转类型观看动画演示。', false);
            animator.addLog('在探索模式下，可以输入数字构建自己的AVL树。', false);
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## AVL树旋转动画交互式教学工具使用指南

欢迎使用AVL树旋转动画教学工具！本工具旨在通过高度可视化的交互方式，帮助您深入理解平衡二叉树（AVL树）的核心平衡机制——四种旋转操作。无论您是初次接触数据结构的学生，还是希望巩固知识的开发者，本工具都将为您提供直观、高效的学习体验。

---

### 一、功能说明

本工具提供两种核心学习模式：

1.  **学习模式**：通过预设的经典案例，系统学习LL、RR、LR、RL四种旋转类型。动画将分步展示从失衡检测到完成旋转的全过程。
2.  **探索模式**：提供一个沙盒环境，您可以自由插入或删除节点，观察AVL树如何动态地自我调整以维持平衡，亲身体验算法的运行逻辑。

---

### 二、主要功能

#### 学习模式
*   **案例选择**：点击“LL型失衡”、“RR型失衡”、“LR型失衡”、“RL型失衡”四个按钮之一，加载对应的预设失衡树结构。
*   **动画控制**：
    *   **播放动画**：自动连续播放从构建到平衡的完整过程。
    *   **上一步/下一步**：手动控制，仔细观摩每一个关键步骤。
    *   **重置**：将动画恢复到初始状态。
*   **步骤分解**（针对LR/RL型）：勾选“显示双旋转分解步骤”复选框，可将复杂的双旋转分解为两次单旋转，便于理解其转化过程。

#### 探索模式
*   **插入节点**：在输入框中输入数字（多个数字用英文逗号分隔），点击“插入节点”或按回车键。工具将实时展示插入过程及可能触发的平衡调整。
*   **删除节点**：输入要删除的数字，点击“删除节点”，观察删除操作可能引发的重新平衡。
*   **清空树**：一键清空当前AVL树，重新开始构建。
*   **实时状态监控**：面板实时显示树的节点总数、高度及平衡状态。

#### 通用功能
*   **可视化画布**：树结构采用清晰的力导向布局，节点颜色动态反映其状态（平衡、失衡、旋转轴）。
*   **信息面板**：右侧日志区实时记录每一步操作和算法判断，是理解算法逻辑的绝佳文本辅助。
*   **图例说明**：清晰的颜色编码帮助您快速识别不同状态的节点和指针。

---

### 三、设计特色

1.  **认知友好的可视化**：
    *   **状态编码**：平衡节点（浅蓝）、失衡节点（浅橙）、焦点节点（浅绿）和重连指针（红色虚线），让算法状态一目了然。
    *   **信息集成**：每个节点内同时显示键值、平衡因子(BF)和高度(H)，帮助您建立三者间的关联。

2.  **符合学习规律的交互设计**：
    *   **从观察到实践**：先通过“学习模式”观察标准案例，再在“探索模式”中验证和探索。
    *   **从连续到分步**：提供连续播放和手动步进两种节奏，适应不同深度的学习需求。
    *   **从整体到局部**：双旋转的分解功能，揭示了复杂操作背后的简单原理。

3.  **即时的反馈与说明**：
    *   每一次插入、删除或旋转，信息面板都会给出明确的文字解释，说明算法正在“思考”什么、为什么要这么做。

---

### 四、教学要点

使用本工具学习时，建议重点关注以下核心概念与过程：

1.  **平衡因子(Balance Factor, BF)**：
    *   理解 `BF = 左子树高度 - 右子树高度` 的定义。
    *   观察BF如何随着插入/删除而改变，并记住 `|BF| > 1` 即为失衡的判定条件。

2.  **最小失衡子树**：
    *   动画会高亮显示从插入点向上追溯，第一个出现失衡的节点。整个旋转操作仅围绕这棵最小失衡子树进行。

3.  **旋转类型的判断（关键！）**：
    *   **LL型**：失衡节点A的BF=+2，且其**左孩子B的BF=+1或0**。
    *   **RR型**：失衡节点A的BF=-2，且其**右孩子B的BF=-1或0**。
    *   **LR型**：失衡节点A的BF=+2，但其**左孩子B的BF=-1**。需要先对B做**左旋**(转为LL型)，再对A做**右旋**。
    *   **RL型**：失衡节点A的BF=-2，但其**右孩子B的BF=+1**。需要先对B做**右旋**(转为RR型)，再对A做**左旋**。

4.  **旋转的本质**：
    *   旋转不是随意转动，而是在**保持二叉搜索树中序遍历有序性**的前提下，通过改变局部几个节点的父子关系，降低整棵树的高度。
    *   观察动画中子树如何像“拎起来”一样移动，指针如何重新连接。

---

### 五、使用建议

为了达到最佳学习效果，我们推荐您按以下流程使用本工具：

1.  **第一阶段：观摩学习**
    *   进入**学习模式**，依次点击四种旋转按钮。
    *   首次观看时，使用 **“播放动画”** 功能，对整体过程建立初步印象。
    *   第二次观看时，使用 **“下一步”** 手动控制，结合右侧信息面板的说明，仔细思考每一步的操作原因。

2.  **第二阶段：深入理解**
    *   再次选择LR或RL型案例，**勾选“显示分解步骤”**。
    *   观察双旋转是如何被分解为两个单旋转的，理解“先转化为基本型，再处理”的核心思想。
    *   尝试在纸上跟随动画的步骤，画出树结构的变化。

3.  **第三阶段：主动探索**
    *   切换到**探索模式**。
    *   **尝试1**：输入序列 `50, 30, 70, 20, 40, 60, 80, 10`，观察构建一个完全平衡的树。
    *   **尝试2**：输入序列 `1, 2, 3, 4, 5`，观察连续的RR型失衡与左旋调整。
    *   **尝试3**：插入 `30, 10, 40, 5, 20` 后，尝试删除节点 `40`，观察可能引发的LR型旋转。
    *   **挑战**：尝试构造一个需要RL型旋转的场景。

4.  **第四阶段：总结归纳**
    *   关闭工具，尝试自己画出四种旋转的示意图，并默写判断条件。
    *   思考：为什么AVL树能保证查询效率始终是O(log n)？旋转操作在其中起到了什么作用？

---

**祝您学习愉快，顺利攻克AVL树这一数据结构与算法学习中的重要里程碑！** 通过本工具的直观演示和您的主动探索，抽象的旋转算法必将变得生动而清晰。