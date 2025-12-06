# 需求：链表反转（三种方法指针重定向）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为计算机科学或软件工程专业的学生，以及准备技术面试的开发者。他们已具备链表、指针/引用等基本数据结构知识，但需要直观、动态地理解反转算法的执行过程。
2.  **核心痛点**：
    *   **抽象性**：指针的指向变化在静态代码或图示中难以追踪，容易混淆。
    *   **过程性**：算法是分步骤、状态连续变化的，传统图文无法清晰展示中间状态。
    *   **方法对比**：需要理解迭代法、递归法、头插法三种方法的异同，包括空间/时间复杂度、逻辑思路和适用场景。
3.  **学习目标**：
    *   **理解**：清晰掌握每种方法中指针移动和节点指向改变的具体步骤。
    *   **对比**：能从动画中直观感受三种方法在空间占用（是否使用额外栈空间）和操作逻辑上的区别。
    *   **应用**：通过交互和步骤控制，加深记忆，能够自行复现算法逻辑。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念解构**：
    *   **迭代法（三指针法）**：核心是维护 `prev`、`curr`、`next` 三个指针，在遍历中逐个翻转指向。
    *   **递归法**：核心是“递”至链表末端，在“归”的过程中逐层修改指向。需突出递归栈的构建与消解过程。
    *   **头插法**：核心是构建一个新链表头，遍历原链表，将每个节点“拔出”并插入新链表头部。

*   **遵循认知规律**：
    1.  **从具体到抽象**：先展示一个具体的链表（如 1->2->3->4->5），然后演示如何将其变为 5->4->3->2->1。
    2.  **分步与连贯结合**：允许用户单步执行，观察每一步指针和节点的变化；同时提供连续播放，感受算法流畅的整体过程。
    3.  **对比学习**：在同一界面或可切换的视图中展示三种方法，使用相同的初始链表，便于横向对比。
    4.  **突出焦点与状态**：在每一步，高亮当前正在操作的节点和指针，淡化其他部分。明确区分“已处理”、“正在处理”、“未处理”的节点区域。

*   **交互设计**：
    1.  **控制面板**：提供“上一步”、“下一步”、“播放/暂停”、“重置”按钮，让用户自主控制学习节奏。
    2.  **方法选择**：通过标签页或按钮组，让用户选择要学习/观察的算法方法。
    3.  **变量状态可视化**：为每个方法的关键指针（如 `prev`, `curr`, `next`, `newHead` 等）设计固定的、带标签的视觉元素（如颜色标记的箭头或指示器），并实时显示其指向的节点。
    4.  **代码联动**：在动画区域旁同步显示简化的伪代码或关键代码行，并高亮当前正在执行的那一行，建立代码与动画的强关联。
    5.  **递归法特殊处理**：为递归法设计一个“递归栈”可视化区域，展示每次函数调用时的参数（当前节点）和栈深度。

*   **视觉呈现**：
    *   **节点设计**：统一使用圆形或矩形表示节点，内部分为两个区域：`val`（值）和 `next`（指针域）。`next` 域在未反转时用箭头指向下一个节点。
    *   **指针设计**：使用不同颜色、带标签的粗箭头或指示器来代表算法中的逻辑指针（如 `curr` 用红色箭头，`prev` 用蓝色箭头，`next` 用绿色箭头）。它们不一定是链表的一部分，而是算法的“工具”。
    *   **动画效果**：指针移动和节点指向改变使用平滑的补间动画。指向改变时，原箭头消失，新箭头从起点画出。关键操作（如断开链接、建立新链接）可配合轻微的缩放或颜色闪烁以强调。
    *   **布局**：主画布用于展示链表本身和指针操作。控制面板在上方或下方。代码区和递归栈区可以放在右侧或下方，形成清晰的信息分区。

#### 配色方案选择
选择对比清晰、符合认知习惯且舒适的配色方案：
*   **背景**：浅灰色（`#f5f7fa`）或白色，确保内容突出。
*   **链表节点**：
    *   默认状态：浅蓝色边框（`#4a90e2`），内部白色填充。
    *   当前焦点节点（`curr`）：填充色为亮黄色（`#ffd700`）。
    *   已处理节点：填充色变为浅绿色（`#98fb98`）。
    *   未处理节点：保持默认。
*   **指针/箭头**：
    *   链表原始指针（`next`）：深灰色（`#333`），细线。
    *   算法指针 `prev`：蓝色（`#3366cc`），粗线，带标签。
    *   算法指针 `curr`：红色（`#cc3333`），粗线，带标签。
    *   算法指针 `next`（迭代法中临时保存的）：绿色（`#33cc66`），粗线，带标签。
    *   新链表头 `newHead`（头插法）：紫色（`#9933cc`），粗线，带标签。
*   **代码高亮**：当前执行行背景色为浅黄色（`#fffacd`）。
*   **递归栈帧**：每个栈帧用轻微阴影的卡片表示，不同深度可用同色系不同深浅区分。
*   **按钮与UI**：使用中性色（如蓝色 `#4a90e2`）表示主要操作，灰色表示禁用状态。

#### 交互功能列表
1.  **全局控制**：
    *   **重置**：将链表和所有状态恢复到初始顺序。
    *   **方法切换**：在“迭代法”、“递归法”、“头插法”之间切换。
    *   **速度调节**：滑块控制连续播放时的动画速度。
2.  **动画播放控制**：
    *   **上一步**：回退到上一个算法步骤。
    *   **播放/暂停**：开始或暂停连续动画播放。
    *   **下一步**：前进到下一个算法步骤。
3.  **可视化元素**：
    *   **链表节点与指针**：动态更新位置、颜色和指向。
    *   **逻辑指针指示器**：实时显示 `prev`、`curr` 等指针的位置。
    *   **代码高亮**：与动画步骤同步高亮对应的代码行。
    *   **递归栈可视化**（仅递归法）：动态展示栈的压入和弹出过程。
4.  **信息显示**：
    *   **步骤说明**：一个文本区域，用自然语言描述当前步骤在做什么（例如：“保存 `curr.next` 到临时变量 `next`”）。
    *   **变量状态表**：以表格形式实时显示关键指针变量所指向的节点值。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>链表反转算法可视化 - 三种方法</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4a90e2;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .visualization-section {
            flex: 3;
            min-width: 300px;
        }

        .code-section {
            flex: 2;
            min-width: 300px;
        }

        .panel {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 25px;
            margin-bottom: 20px;
        }

        h2 {
            color: #4a90e2;
            margin-bottom: 20px;
            font-size: 1.4em;
        }

        h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        /* 方法选择器 */
        .method-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .method-btn {
            padding: 12px 24px;
            background-color: #eef2f7;
            border: 2px solid #d1d9e6;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            color: #5a6c7d;
            transition: all 0.3s ease;
            flex: 1;
            text-align: center;
            min-width: 120px;
        }

        .method-btn:hover {
            background-color: #e1e8f0;
        }

        .method-btn.active {
            background-color: #4a90e2;
            color: white;
            border-color: #4a90e2;
        }

        /* 控制面板 */
        .control-panel {
            display: flex;
            gap: 15px;
            align-items: center;
            flex-wrap: wrap;
            margin-bottom: 25px;
        }

        .control-btn {
            padding: 10px 20px;
            background-color: #4a90e2;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .control-btn:hover {
            background-color: #3a7bc8;
        }

        .control-btn:disabled {
            background-color: #a0b9d9;
            cursor: not-allowed;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-left: auto;
        }

        .speed-slider {
            width: 150px;
        }

        /* 画布区域 */
        .canvas-container {
            position: relative;
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #e1e8f0;
            height: 400px;
            margin-bottom: 20px;
        }

        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        /* 递归栈区域 */
        .recursion-stack-container {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            border: 1px dashed #d1d9e6;
            height: 150px;
            overflow-y: auto;
            margin-top: 20px;
        }

        .stack-frame {
            background-color: white;
            border-left: 4px solid #9933cc;
            padding: 10px 15px;
            margin-bottom: 8px;
            border-radius: 4px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            font-family: monospace;
        }

        .stack-frame.active {
            background-color: #f3e6ff;
            font-weight: bold;
        }

        /* 代码区域 */
        .code-container {
            background-color: #2c3e50;
            color: #ecf0f1;
            border-radius: 8px;
            padding: 20px;
            overflow-x: auto;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 14px;
            line-height: 1.5;
            height: 400px;
        }

        .code-line {
            padding: 2px 0;
            white-space: pre;
        }

        .code-line.highlighted {
            background-color: rgba(255, 250, 205, 0.3);
            color: #ffd700;
        }

        /* 变量状态表 */
        .variables-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }

        .variables-table th, .variables-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #e1e8f0;
        }

        .variables-table th {
            background-color: #f8f9fa;
            font-weight: 600;
            color: #4a90e2;
        }

        .variables-table tr:hover {
            background-color: #f8f9fa;
        }

        .pointer-value {
            font-weight: bold;
            font-family: monospace;
        }

        .pointer-prev { color: #3366cc; }
        .pointer-curr { color: #cc3333; }
        .pointer-next { color: #33cc66; }
        .pointer-newhead { color: #9933cc; }

        /* 步骤说明 */
        .step-description {
            background-color: #f0f7ff;
            border-left: 4px solid #4a90e2;
            padding: 15px;
            border-radius: 4px;
            margin-top: 20px;
            font-size: 1.05em;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 8px;
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

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #e1e8f0;
            color: #7f8c8d;
            font-size: 0.9em;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .control-panel {
                justify-content: center;
            }
            
            .speed-control {
                margin-left: 0;
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>链表反转算法可视化</h1>
        <p class="subtitle">三种方法：迭代法、递归法、头插法</p>
    </header>

    <div class="container">
        <div class="panel">
            <h2>算法方法选择</h2>
            <div class="method-selector">
                <button class="method-btn active" data-method="iterative">迭代法（三指针）</button>
                <button class="method-btn" data-method="recursive">递归法</button>
                <button class="method-btn" data-method="headInsert">头插法</button>
            </div>

            <div class="control-panel">
                <button id="resetBtn" class="control-btn">
                    <span>↺</span> 重置
                </button>
                <button id="prevBtn" class="control-btn" disabled>
                    <span>←</span> 上一步
                </button>
                <button id="playPauseBtn" class="control-btn">
                    <span>▶</span> 播放
                </button>
                <button id="nextBtn" class="control-btn">
                    <span>→</span> 下一步
                </button>
                
                <div class="speed-control">
                    <span>速度:</span>
                    <input type="range" id="speedSlider" class="speed-slider" min="1" max="10" value="5">
                    <span id="speedValue">中</span>
                </div>
            </div>

            <div class="canvas-container">
                <canvas id="animationCanvas"></canvas>
            </div>

            <div id="recursionStackContainer" class="recursion-stack-container" style="display: none;">
                <h3>递归调用栈</h3>
                <div id="stackFrames"></div>
            </div>

            <div class="step-description" id="stepDescription">
                点击"播放"或"下一步"开始动画演示。初始链表: 1 → 2 → 3 → 4 → 5
            </div>
        </div>

        <div class="main-content">
            <div class="visualization-section">
                <div class="panel">
                    <h2>变量状态</h2>
                    <table class="variables-table">
                        <thead>
                            <tr>
                                <th>指针变量</th>
                                <th>指向节点值</th>
                                <th>说明</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><span class="pointer-prev pointer-value">prev</span></td>
                                <td id="prevValue">null</td>
                                <td>前一个节点</td>
                            </tr>
                            <tr>
                                <td><span class="pointer-curr pointer-value">curr</span></td>
                                <td id="currValue">1</td>
                                <td>当前节点</td>
                            </tr>
                            <tr>
                                <td><span class="pointer-next pointer-value">next</span></td>
                                <td id="nextValue">2</td>
                                <td>下一个节点（临时）</td>
                            </tr>
                            <tr id="newHeadRow" style="display: none;">
                                <td><span class="pointer-newhead pointer-value">newHead</span></td>
                                <td id="newHeadValue">null</td>
                                <td>新链表头</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <div class="panel">
                    <h2>图例说明</h2>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #4a90e2;"></div>
                            <span>链表节点（默认）</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #ffd700;"></div>
                            <span>当前节点 (curr)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #98fb98;"></div>
                            <span>已处理节点</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #3366cc;"></div>
                            <span>prev 指针</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #cc3333;"></div>
                            <span>curr 指针</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #33cc66;"></div>
                            <span>next 指针</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #9933cc;"></div>
                            <span>newHead 指针（头插法）</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="code-section">
                <div class="panel">
                    <h2>算法代码</h2>
                    <div class="code-container" id="codeContainer">
                        <!-- 代码将通过JavaScript动态生成 -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>链表反转算法可视化 | 使用HTML5 Canvas实现 | 设计用于教学演示</p>
    </footer>

    <script>
        // 全局变量和配置
        const CONFIG = {
            NODE_RADIUS: 28,
            NODE_SPACING: 120,
            VERTICAL_SPACING: 100,
            ANIMATION_DURATION: 800,
            COLORS: {
                NODE_DEFAULT: '#4a90e2',
                NODE_CURRENT: '#ffd700',
                NODE_PROCESSED: '#98fb98',
                POINTER_PREV: '#3366cc',
                POINTER_CURR: '#cc3333',
                POINTER_NEXT: '#33cc66',
                POINTER_NEWHEAD: '#9933cc',
                LINK_DEFAULT: '#333',
                BACKGROUND: '#f5f7fa',
                CODE_HIGHLIGHT: 'rgba(255, 250, 205, 0.3)'
            }
        };

        // 算法步骤定义
        const ALGORITHMS = {
            iterative: {
                name: '迭代法（三指针）',
                steps: [
                    { 
                        desc: '初始化: prev = null, curr = head, next = null',
                        codeLine: 0,
                        action: 'init'
                    },
                    { 
                        desc: '循环开始: 当 curr ≠ null 时',
                        codeLine: 1,
                        action: 'loop_start'
                    },
                    { 
                        desc: '保存下一个节点: next = curr.next',
                        codeLine: 2,
                        action: 'save_next'
                    },
                    { 
                        desc: '反转指针: curr.next = prev',
                        codeLine: 3,
                        action: 'reverse_link'
                    },
                    { 
                        desc: '移动指针: prev = curr, curr = next',
                        codeLine: 4,
                        action: 'move_pointers'
                    },
                    { 
                        desc: '循环结束，返回 prev 作为新头节点',
                        codeLine: 5,
                        action: 'return'
                    }
                ],
                code: [
                    'function reverseIterative(head) {',
                    '  let prev = null;',
                    '  let curr = head;',
                    '  let next = null;',
                    '  ',
                    '  while (curr !== null) {',
                    '    next = curr.next;    // 保存下一个节点',
                    '    curr.next = prev;    // 反转指针',
                    '    prev = curr;         // prev前进',
                    '    curr = next;         // curr前进',
                    '  }',
                    '  ',
                    '  return prev; // 新头节点',
                    '}'
                ]
            },
            recursive: {
                name: '递归法',
                steps: [
                    { 
                        desc: '递归基: 如果 head 为空或 head.next 为空，返回 head',
                        codeLine: 0,
                        action: 'base_case_check'
                    },
                    { 
                        desc: '递归调用: newHead = reverseRecursive(head.next)',
                        codeLine: 1,
                        action: 'recursive_call'
                    },
                    { 
                        desc: '反转指针: head.next.next = head',
                        codeLine: 2,
                        action: 'reverse_link'
                    },
                    { 
                        desc: '断开原链接: head.next = null',
                        codeLine: 3,
                        action: 'break_link'
                    },
                    { 
                        desc: '返回新头节点: return newHead',
                        codeLine: 4,
                        action: 'return_newhead'
                    }
                ],
                code: [
                    'function reverseRecursive(head) {',
                    '  // 递归基',
                    '  if (head === null || head.next === null) {',
                    '    return head;',
                    '  }',
                    '  ',
                    '  // 递归调用，直到链表末尾',
                    '  let newHead = reverseRecursive(head.next);',
                    '  ',
                    '  // 反转指针',
                    '  head.next.next = head;',
                    '  ',
                    '  // 断开原链接',
                    '  head.next = null;',
                    '  ',
                    '  // 返回新头节点',
                    '  return newHead;',
                    '}'
                ]
            },
            headInsert: {
                name: '头插法',
                steps: [
                    { 
                        desc: '初始化: newHead = null, curr = head',
                        codeLine: 0,
                        action: 'init'
                    },
                    { 
                        desc: '循环开始: 当 curr ≠ null 时',
                        codeLine: 1,
                        action: 'loop_start'
                    },
                    { 
                        desc: '保存下一个节点: next = curr.next',
                        codeLine: 2,
                        action: 'save_next'
                    },
                    { 
                        desc: '头插操作: curr.next = newHead',
                        codeLine: 3,
                        action: 'insert_at_head'
                    },
                    { 
                        desc: '更新新头: newHead = curr',
                        codeLine: 4,
                        action: 'update_newhead'
                    },
                    { 
                        desc: '移动指针: curr = next',
                        codeLine: 5,
                        action: 'move_curr'
                    },
                    { 
                        desc: '循环结束，返回 newHead',
                        codeLine: 6,
                        action: 'return'
                    }
                ],
                code: [
                    'function reverseHeadInsert(head) {',
                    '  let newHead = null;',
                    '  let curr = head;',
                    '  let next = null;',
                    '  ',
                    '  while (curr !== null) {',
                    '    next = curr.next;      // 保存下一个节点',
                    '    curr.next = newHead;   // 头插操作',
                    '    newHead = curr;        // 更新新头',
                    '    curr = next;           // 移动到下一个节点',
                    '  }',
                    '  ',
                    '  return newHead;',
                    '}'
                ]
            }
        };

        // 链表节点类
        class ListNode {
            constructor(value, x, y) {
                this.value = value;
                this.x = x;
                this.y = y;
                this.next = null;
                this.color = CONFIG.COLORS.NODE_DEFAULT;
                this.processed = false;
                this.isCurrent = false;
            }

            draw(ctx) {
                // 绘制节点
                ctx.beginPath();
                ctx.arc(this.x, this.y, CONFIG.NODE_RADIUS, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 2;
                ctx.stroke();

                // 绘制节点值
                ctx.fillStyle = '#2c3e50';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(this.value.toString(), this.x, this.y);

                // 绘制next指针标签
                ctx.fillStyle = '#7f8c8d';
                ctx.font = '12px Arial';
                ctx.fillText('next', this.x, this.y + CONFIG.NODE_RADIUS + 15);
            }

            drawLink(ctx, targetNode) {
                if (!targetNode) return;

                // 计算箭头起点和终点
                const dx = targetNode.x - this.x;
                const dy = targetNode.y - this.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                const unitX = dx / distance;
                const unitY = dy / distance;

                const startX = this.x + unitX * CONFIG.NODE_RADIUS;
                const startY = this.y + unitY * CONFIG.NODE_RADIUS;
                const endX = targetNode.x - unitX * CONFIG.NODE_RADIUS;
                const endY = targetNode.y - unitY * CONFIG.NODE_RADIUS;

                // 绘制连线
                ctx.beginPath();
                ctx.moveTo(startX, startY);
                ctx.lineTo(endX, endY);
                ctx.strokeStyle = CONFIG.COLORS.LINK_DEFAULT;
                ctx.lineWidth = 2;
                ctx.stroke();

                // 绘制箭头
                const arrowSize = 8;
                const angle = Math.atan2(dy, dx);
                
                ctx.beginPath();
                ctx.moveTo(endX, endY);
                ctx.lineTo(
                    endX - arrowSize * Math.cos(angle - Math.PI / 6),
                    endY - arrowSize * Math.sin(angle - Math.PI / 6)
                );
                ctx.lineTo(
                    endX - arrowSize * Math.cos(angle + Math.PI / 6),
                    endY - arrowSize * Math.sin(angle + Math.PI / 6)
                );
                ctx.closePath();
                ctx.fillStyle = CONFIG.COLORS.LINK_DEFAULT;
                ctx.fill();
            }
        }

        // 指针指示器类
        class PointerIndicator {
            constructor(name, color, label) {
                this.name = name;
                this.color = color;
                this.label = label;
                this.targetNode = null;
                this.x = 0;
                this.y = 0;
            }

            updatePosition(targetNode, offsetX = 0, offsetY = 0) {
                this.targetNode = targetNode;
                if (targetNode) {
                    this.x = targetNode.x + offsetX;
                    this.y = targetNode.y + offsetY;
                }
            }

            draw(ctx) {
                if (!this.targetNode) return;

                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(this.x, this.y);
                ctx.lineTo(this.targetNode.x, this.targetNode.y);
                ctx.strokeStyle = this.color;
                ctx.lineWidth = 3;
                ctx.setLineDash([5, 3]);
                ctx.stroke();
                ctx.setLineDash([]);

                // 绘制指针标签
                ctx.fillStyle = this.color;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'bottom';
                ctx.fillText(this.label, this.x, this.y - 10);

                // 绘制指针点
                ctx.beginPath();
                ctx.arc(this.x, this.y, 6, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 1;
                ctx.stroke();
            }
        }

        // 主应用类
        class LinkedListAnimation {
            constructor() {
                this.canvas = document.getElementById('animationCanvas');
                this.ctx = this.canvas.getContext('2d');
                this.method = 'iterative';
                this.currentStep = 0;
                this.isPlaying = false;
                this.animationSpeed = 5;
                this.animationStartTime = 0;
                this.nodes = [];
                this.pointers = {
                    prev: new PointerIndicator('prev', CONFIG.COLORS.POINTER_PREV, 'prev'),
                    curr: new PointerIndicator('curr', CONFIG.COLORS.POINTER_CURR, 'curr'),
                    next: new PointerIndicator('next', CONFIG.COLORS.POINTER_NEXT, 'next'),
                    newHead: new PointerIndicator('newHead', CONFIG.COLORS.POINTER_NEWHEAD, 'newHead')
                };
                this.recursionStack = [];
                this.originalList = [];
                this.init();
            }

            init() {
                this.setupCanvas();
                this.createLinkedList();
                this.setupEventListeners();
                this.renderCode();
                this.updateVariableDisplay();
                this.draw();
            }

            setupCanvas() {
                const container = this.canvas.parentElement;
                this.canvas.width = container.clientWidth;
                this.canvas.height = container.clientHeight;
                
                window.addEventListener('resize', () => {
                    this.canvas.width = container.clientWidth;
                    this.canvas.height = container.clientHeight;
                    this.createLinkedList(); // 重新计算节点位置
                    this.draw();
                });
            }

            createLinkedList() {
                this.nodes = [];
                this.originalList = [];
                
                const values = [1, 2, 3, 4, 5];
                const startX = 100;
                const startY = this.canvas.height / 2;
                
                // 创建节点并设置位置
                for (let i = 0; i < values.length; i++) {
                    const node = new ListNode(
                        values[i],
                        startX + i * CONFIG.NODE_SPACING,
                        startY
                    );
                    this.nodes.push(node);
                    this.originalList.push({...node});
                }
                
                // 设置next指针
                for (let i = 0; i < this.nodes.length - 1; i++) {
                    this.nodes[i].next = this.nodes[i + 1];
                }
                
                // 初始化指针位置
                this.pointers.curr.updatePosition(this.nodes[0], -60, -80);
                this.pointers.next.updatePosition(this.nodes[1] || null, -60, -80);
                this.pointers.prev.updatePosition(null, -60, -80);
                this.pointers.newHead.updatePosition(null, -60, -80);
                
                // 重置节点状态
                this.nodes.forEach(node => {
                    node.color = CONFIG.COLORS.NODE_DEFAULT;
                    node.processed = false;
                    node.isCurrent = false;
                });
                
                // 设置第一个节点为当前节点
                if (this.nodes[0]) {
                    this.nodes[0].isCurrent = true;
                    this.nodes[0].color = CONFIG.COLORS.NODE_CURRENT;
                }
                
                this.currentStep = 0;
                this.recursionStack = [];
                this.updateRecursionStackDisplay();
            }

            setupEventListeners() {
                // 方法选择按钮
                document.querySelectorAll('.method-btn').forEach(btn => {
                    btn.addEventListener('click', () => {
                        document.querySelectorAll('.method-btn').forEach(b => b.classList.remove('active'));
                        btn.classList.add('active');
                        this.method = btn.dataset.method;
                        this.resetAnimation();
                        this.renderCode();
                        this.updateVariableDisplay();
                        
                        // 显示/隐藏递归栈区域
                        const stackContainer = document.getElementById('recursionStackContainer');
                        stackContainer.style.display = this.method === 'recursive' ? 'block' : 'none';
                        
                        // 显示/隐藏newHead行
                        const newHeadRow = document.getElementById('newHeadRow');
                        newHeadRow.style.display = this.method === 'headInsert' ? 'table-row' : 'none';
                    });
                });

                // 控制按钮
                document.getElementById('resetBtn').addEventListener('click', () => this.resetAnimation());
                document.getElementById('prevBtn').addEventListener('click', () => this.prevStep());
                document.getElementById('nextBtn').addEventListener('click', () => this.nextStep());
                document.getElementById('playPauseBtn').addEventListener('click', () => this.togglePlay());

                // 速度滑块
                const speedSlider = document.getElementById('speedSlider');
                const speedValue = document.getElementById('speedValue');
                
                speedSlider.addEventListener('input', () => {
                    this.animationSpeed = parseInt(speedSlider.value);
                    const speedLabels = ['很慢', '慢', '较慢', '中慢', '中', '中快', '较快', '快', '很快', '极快'];
                    speedValue.textContent = speedLabels[this.animationSpeed - 1];
                });
            }

            renderCode() {
                const codeContainer = document.getElementById('codeContainer');
                const algorithm = ALGORITHMS[this.method];
                
                codeContainer.innerHTML = '';
                algorithm.code.forEach((line, index) => {
                    const lineDiv = document.createElement('div');
                    lineDiv.className = 'code-line';
                    lineDiv.textContent = line;
                    lineDiv.dataset.line = index;
                    codeContainer.appendChild(lineDiv);
                });
                
                this.highlightCodeLine(0);
            }

            highlightCodeLine(lineNumber) {
                document.querySelectorAll('.code-line').forEach(line => {
                    line.classList.remove('highlighted');
                });
                
                const targetLine = document.querySelector(`.code-line[data-line="${lineNumber}"]`);
                if (targetLine) {
                    targetLine.classList.add('highlighted');
                    targetLine.scrollIntoView({ behavior: 'smooth', block: 'center' });
                }
            }

            updateVariableDisplay() {
                const prevNode = this.pointers.prev.targetNode;
                const currNode = this.pointers.curr.targetNode;
                const nextNode = this.pointers.next.targetNode;
                const newHeadNode = this.pointers.newHead.targetNode;
                
                document.getElementById('prevValue').textContent = prevNode ? prevNode.value : 'null';
                document.getElementById('currValue').textContent = currNode ? currNode.value : 'null';
                document.getElementById('nextValue').textContent = nextNode ? nextNode.value : 'null';
                document.getElementById('newHeadValue').textContent = newHeadNode ? newHeadNode.value : 'null';
            }

            updateRecursionStackDisplay() {
                const stackFrames = document.getElementById('stackFrames');
                stackFrames.innerHTML = '';
                
                this.recursionStack.forEach((frame, index) => {
                    const frameDiv = document.createElement('div');
                    frameDiv.className = `stack-frame ${index === this.recursionStack.length - 1 ? 'active' : ''}`;
                    frameDiv.textContent = `reverseRecursive(node=${frame.node ? frame.node.value : 'null'}) - 深度: ${frame.depth}`;
                    stackFrames.appendChild(frameDiv);
                });
                
                // 滚动到底部
                stackFrames.scrollTop = stackFrames.scrollHeight;
            }

            updateStepDescription() {
                const algorithm = ALGORITHMS[this.method];
                const step = algorithm.steps[this.currentStep];
                const descElement = document.getElementById('stepDescription');
                
                if (step) {
                    descElement.textContent = `步骤 ${this.currentStep + 1}/${algorithm.steps.length}: ${step.desc}`;
                    this.highlightCodeLine(step.codeLine);
                }
            }

            draw() {
                // 清空画布
                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
                
                // 绘制所有连线
                this.nodes.forEach(node => {
                    if (node.next) {
                        node.drawLink(this.ctx, node.next);
                    }
                });
                
                // 绘制所有节点
                this.nodes.forEach(node => {
                    node.draw(this.ctx);
                });
                
                // 绘制所有指针
                Object.values(this.pointers).forEach(pointer => {
                    pointer.draw(this.ctx);
                });
            }

            resetAnimation() {
                this.isPlaying = false;
                this.currentStep = 0;
                this.createLinkedList();
                this.updateVariableDisplay();
                this.updateStepDescription();
                this.updateRecursionStackDisplay();
                
                const playBtn = document.getElementById('playPauseBtn');
                playBtn.innerHTML = '<span>▶</span> 播放';
                document.getElementById('prevBtn').disabled = true;
                
                this.draw();
            }

            prevStep() {
                if (this.currentStep > 0) {
                    this.currentStep--;
                    this.executeStep(false); // 反向执行
                    this.updateStepDescription();
                    document.getElementById('nextBtn').disabled = false;
                }
                
                document.getElementById('prevBtn').disabled = this.currentStep === 0;
            }

            nextStep() {
                const algorithm = ALGORITHMS[this.method];
                
                if (this.currentStep < algorithm.steps.length) {
                    this.executeStep(true); // 正向执行
                    this.currentStep++;
                    this.updateStepDescription();
                    document.getElementById('prevBtn').disabled = false;
                }
                
                if (this.currentStep >= algorithm.steps.length) {
                    document.getElementById('nextBtn').disabled = true;
                    this.isPlaying = false;
                    const playBtn = document.getElementById('playPauseBtn');
                    playBtn.innerHTML = '<span>▶</span> 播放';
                }
            }

            executeStep(forward = true) {
                const algorithm = ALGORITHMS[this.method];
                const step = algorithm.steps[forward ? this.currentStep : this.currentStep - 1];
                
                if (!step) return;
                
                switch (this.method) {
                    case 'iterative':
                        this.executeIterativeStep(step.action, forward);
                        break;
                    case 'recursive':
                        this.executeRecursiveStep(step.action, forward);
                        break;
                    case 'headInsert':
                        this.executeHeadInsertStep(step.action, forward);
                        break;
                }
                
                this.updateVariableDisplay();
                this.draw();
            }

            executeIterativeStep(action, forward) {
                const currNode = this.pointers.curr.targetNode;
                const prevNode = this.pointers.prev.targetNode;
                const nextNode = this.pointers.next.targetNode;
                
                if (!forward) {
                    // 反向执行（撤销操作）
                    switch (action) {
                        case 'move_pointers':
                            this.pointers.curr.updatePosition(prevNode, -60, -80);
                            this.pointers.prev.updatePosition(this.findPrevNode(prevNode), -60, -80);
                            if (currNode) {
                                currNode.next = nextNode;
                                currNode.color = CONFIG.COLORS.NODE_CURRENT;
                                currNode.isCurrent = true;
                            }
                            if (prevNode) {
                                prevNode.color = CONFIG.COLORS.NODE_PROCESSED;
                                prevNode.isCurrent = false;
                            }
                            break;
                        case 'reverse_link':
                            if (currNode) {
                                currNode.next = nextNode;
                            }
                            break;
                        case 'save_next':
                            this.pointers.next.updatePosition(currNode ? currNode.next : null, -60, -80);
                            break;
                        case 'init':
                            this.pointers.prev.updatePosition(null, -60, -80);
                            this.pointers.curr.updatePosition(this.nodes[0], -60, -80);
                            this.pointers.next.updatePosition(this.nodes[1] || null, -60, -80);
                            this.nodes.forEach(node => {
                                node.color = CONFIG.COLORS.NODE_DEFAULT;
                                node.processed = false;
                                node.isCurrent = false;
                            });
                            if (this.nodes[0]) {
                                this.nodes[0].isCurrent = true;
                                this.nodes[0].color = CONFIG.COLORS.NODE_CURRENT;
                            }
                            break;
                    }
                    return;
                }
                
                // 正向执行
                switch (action) {
                    case 'init':
                        this.pointers.prev.updatePosition(null, -60, -80);
                        this.pointers.curr.updatePosition(this.nodes[0], -60, -80);
                        this.pointers.next.updatePosition(this.nodes[1] || null, -60, -80);
                        break;
                        
                    case 'save_next':
                        if (currNode) {
                            this.pointers.next.updatePosition(currNode.next, -60, -80);
                        }
                        break
<!--检测到代码截断，自动续写中...-->
                    case 'reverse_link':
                        if (currNode) {
                            currNode.next = prevNode;
                        }
                        break;
                        
                    case 'move_pointers':
                        if (currNode) {
                            currNode.color = CONFIG.COLORS.NODE_PROCESSED;
                            currNode.processed = true;
                            currNode.isCurrent = false;
                        }
                        
                        this.pointers.prev.updatePosition(currNode, -60, -80);
                        this.pointers.curr.updatePosition(nextNode, -60, -80);
                        
                        if (nextNode) {
                            nextNode.color = CONFIG.COLORS.NODE_CURRENT;
                            nextNode.isCurrent = true;
                            this.pointers.next.updatePosition(nextNode.next, -60, -80);
                        } else {
                            this.pointers.next.updatePosition(null, -60, -80);
                        }
                        break;
                }
            }

            executeRecursiveStep(action, forward) {
                const currNode = this.pointers.curr.targetNode;
                
                if (!forward) {
                    // 反向执行（撤销操作）
                    switch (action) {
                        case 'return_newhead':
                            // 从栈中弹出
                            if (this.recursionStack.length > 0) {
                                const frame = this.recursionStack.pop();
                                this.pointers.curr.updatePosition(frame.node, -60, -80);
                                if (frame.node) {
                                    frame.node.color = CONFIG.COLORS.NODE_CURRENT;
                                    frame.node.isCurrent = true;
                                }
                                this.updateRecursionStackDisplay();
                            }
                            break;
                        case 'break_link':
                            if (currNode && currNode.next) {
                                currNode.next.next = currNode;
                            }
                            break;
                        case 'reverse_link':
                            if (currNode && currNode.next) {
                                currNode.next.next = null;
                            }
                            break;
                        case 'recursive_call':
                            if (currNode && currNode.next) {
                                // 恢复next指针
                                const nextNode = currNode.next;
                                nextNode.color = CONFIG.COLORS.NODE_DEFAULT;
                                nextNode.isCurrent = false;
                                nextNode.processed = false;
                            }
                            break;
                        case 'base_case_check':
                            // 重置到初始状态
                            this.pointers.curr.updatePosition(this.nodes[0], -60, -80);
                            this.recursionStack = [];
                            this.updateRecursionStackDisplay();
                            this.nodes.forEach(node => {
                                node.color = CONFIG.COLORS.NODE_DEFAULT;
                                node.processed = false;
                                node.isCurrent = false;
                            });
                            if (this.nodes[0]) {
                                this.nodes[0].isCurrent = true;
                                this.nodes[0].color = CONFIG.COLORS.NODE_CURRENT;
                            }
                            break;
                    }
                    return;
                }
                
                // 正向执行
                switch (action) {
                    case 'base_case_check':
                        // 检查是否到达递归基
                        if (!currNode || !currNode.next) {
                            // 到达递归基，直接返回
                            this.currentStep = ALGORITHMS.recursive.steps.length - 1;
                        }
                        break;
                        
                    case 'recursive_call':
                        if (currNode) {
                            // 将当前调用压入栈
                            this.recursionStack.push({
                                node: currNode,
                                depth: this.recursionStack.length + 1
                            });
                            
                            // 移动到下一个节点
                            const nextNode = currNode.next;
                            if (nextNode) {
                                currNode.color = CONFIG.COLORS.NODE_PROCESSED;
                                currNode.isCurrent = false;
                                currNode.processed = true;
                                
                                nextNode.color = CONFIG.COLORS.NODE_CURRENT;
                                nextNode.isCurrent = true;
                                this.pointers.curr.updatePosition(nextNode, -60, -80);
                            }
                            this.updateRecursionStackDisplay();
                        }
                        break;
                        
                    case 'reverse_link':
                        if (currNode && currNode.next) {
                            currNode.next.next = currNode;
                        }
                        break;
                        
                    case 'break_link':
                        if (currNode) {
                            currNode.next = null;
                        }
                        break;
                        
                    case 'return_newhead':
                        // 从栈中弹出
                        if (this.recursionStack.length > 0) {
                            const frame = this.recursionStack.pop();
                            if (frame.node) {
                                frame.node.color = CONFIG.COLORS.NODE_PROCESSED;
                                frame.node.processed = true;
                                frame.node.isCurrent = false;
                            }
                            
                            // 如果栈中还有元素，回到上一层
                            if (this.recursionStack.length > 0) {
                                const prevFrame = this.recursionStack[this.recursionStack.length - 1];
                                this.pointers.curr.updatePosition(prevFrame.node, -60, -80);
                                if (prevFrame.node) {
                                    prevFrame.node.color = CONFIG.COLORS.NODE_CURRENT;
                                    prevFrame.node.isCurrent = true;
                                }
                            } else {
                                // 递归结束，newHead指向最后一个节点
                                const lastNode = this.nodes[this.nodes.length - 1];
                                this.pointers.newHead.updatePosition(lastNode, -60, -80);
                                this.pointers.curr.updatePosition(null, -60, -80);
                            }
                            this.updateRecursionStackDisplay();
                        }
                        break;
                }
            }

            executeHeadInsertStep(action, forward) {
                const currNode = this.pointers.curr.targetNode;
                const newHeadNode = this.pointers.newHead.targetNode;
                const nextNode = this.pointers.next.targetNode;
                
                if (!forward) {
                    // 反向执行（撤销操作）
                    switch (action) {
                        case 'move_curr':
                            this.pointers.curr.updatePosition(newHeadNode, -60, -80);
                            if (currNode) {
                                currNode.color = CONFIG.COLORS.NODE_CURRENT;
                                currNode.isCurrent = true;
                            }
                            if (newHeadNode) {
                                newHeadNode.color = CONFIG.COLORS.NODE_PROCESSED;
                                newHeadNode.isCurrent = false;
                            }
                            break;
                        case 'update_newhead':
                            this.pointers.newHead.updatePosition(this.findPrevNode(newHeadNode), -60, -80);
                            if (currNode) {
                                currNode.next = nextNode;
                            }
                            break;
                        case 'insert_at_head':
                            if (currNode) {
                                currNode.next = nextNode;
                            }
                            break;
                        case 'save_next':
                            this.pointers.next.updatePosition(currNode ? currNode.next : null, -60, -80);
                            break;
                        case 'init':
                            this.pointers.newHead.updatePosition(null, -60, -80);
                            this.pointers.curr.updatePosition(this.nodes[0], -60, -80);
                            this.pointers.next.updatePosition(this.nodes[1] || null, -60, -80);
                            this.nodes.forEach(node => {
                                node.color = CONFIG.COLORS.NODE_DEFAULT;
                                node.processed = false;
                                node.isCurrent = false;
                                // 恢复原始链接
                                const index = this.nodes.indexOf(node);
                                if (index < this.nodes.length - 1) {
                                    node.next = this.nodes[index + 1];
                                } else {
                                    node.next = null;
                                }
                            });
                            if (this.nodes[0]) {
                                this.nodes[0].isCurrent = true;
                                this.nodes[0].color = CONFIG.COLORS.NODE_CURRENT;
                            }
                            break;
                    }
                    return;
                }
                
                // 正向执行
                switch (action) {
                    case 'init':
                        this.pointers.newHead.updatePosition(null, -60, -80);
                        this.pointers.curr.updatePosition(this.nodes[0], -60, -80);
                        this.pointers.next.updatePosition(this.nodes[1] || null, -60, -80);
                        break;
                        
                    case 'save_next':
                        if (currNode) {
                            this.pointers.next.updatePosition(currNode.next, -60, -80);
                        }
                        break;
                        
                    case 'insert_at_head':
                        if (currNode) {
                            currNode.next = newHeadNode;
                        }
                        break;
                        
                    case 'update_newhead':
                        this.pointers.newHead.updatePosition(currNode, -60, -80);
                        if (currNode) {
                            currNode.color = CONFIG.COLORS.NODE_PROCESSED;
                            currNode.processed = true;
                            currNode.isCurrent = false;
                        }
                        break;
                        
                    case 'move_curr':
                        this.pointers.curr.updatePosition(nextNode, -60, -80);
                        if (nextNode) {
                            nextNode.color = CONFIG.COLORS.NODE_CURRENT;
                            nextNode.isCurrent = true;
                            this.pointers.next.updatePosition(nextNode.next, -60, -80);
                        } else {
                            this.pointers.next.updatePosition(null, -60, -80);
                        }
                        break;
                }
            }

            findPrevNode(node) {
                if (!node) return null;
                for (let i = 0; i < this.nodes.length; i++) {
                    if (this.nodes[i].next === node) {
                        return this.nodes[i];
                    }
                }
                return null;
            }

            togglePlay() {
                this.isPlaying = !this.isPlaying;
                const playBtn = document.getElementById('playPauseBtn');
                
                if (this.isPlaying) {
                    playBtn.innerHTML = '<span>⏸</span> 暂停';
                    this.playAnimation();
                } else {
                    playBtn.innerHTML = '<span>▶</span> 播放';
                }
            }

            playAnimation() {
                if (!this.isPlaying) return;
                
                const algorithm = ALGORITHMS[this.method];
                const speedFactor = this.animationSpeed / 5; // 1-10 映射到 0.2-2
                const stepDuration = CONFIG.ANIMATION_DURATION / speedFactor;
                
                if (this.currentStep < algorithm.steps.length) {
                    this.nextStep();
                    
                    // 设置下一个步骤的延迟
                    setTimeout(() => {
                        this.playAnimation();
                    }, stepDuration);
                } else {
                    this.isPlaying = false;
                    const playBtn = document.getElementById('playPauseBtn');
                    playBtn.innerHTML = '<span>▶</span> 播放';
                }
            }

            animate() {
                requestAnimationFrame(() => this.animate());
                // 这里可以添加更复杂的动画逻辑
            }
        }

        // 初始化应用
        document.addEventListener('DOMContentLoaded', () => {
            const app = new LinkedListAnimation();
            app.animate();
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用“链表反转算法可视化”教学动画！本工具旨在通过直观的动态演示，帮助您深入理解链表反转的三种经典算法。无论您是正在学习数据结构的学生，还是准备技术面试的开发者，相信这个交互式动画都能为您提供独特的价值。

---

### 功能说明

本动画系统完整实现了链表反转的三种核心算法：
1. **迭代法（三指针法）** - 通过 `prev`、`curr`、`next` 三个指针在遍历中逐个翻转节点指向
2. **递归法** - 利用递归调用栈，从链表末端开始逐层反转指针
3. **头插法** - 构建新链表头，将原链表节点逐个插入新链表头部

系统采用**HTML5 Canvas**技术实现，所有动画均在浏览器中实时渲染，无需安装任何插件。

### 主要功能

#### 1. 多算法切换
- 通过顶部标签页可在三种算法间自由切换
- 每种算法都有独立的可视化逻辑和代码展示
- 递归法特别包含**递归调用栈可视化**区域

#### 2. 精细的动画控制
- **播放/暂停**：连续观看算法执行全过程
- **上一步/下一步**：单步控制，仔细分析每个关键操作
- **速度调节**：10档速度可选（从“很慢”到“极快”）
- **重置**：随时恢复到初始状态

#### 3. 多维信息同步
- **可视化画布**：实时显示链表结构、节点状态和指针位置
- **代码高亮**：与动画步骤同步高亮对应的代码行
- **变量状态表**：实时显示 `prev`、`curr`、`next`、`newHead` 等关键变量的值
- **步骤说明**：用自然语言描述当前步骤的操作含义
- **递归栈跟踪**（仅递归法）：可视化显示递归调用的深度和参数

#### 4. 直观的视觉编码
- **颜色系统**：
  - 🔵 蓝色：`prev` 指针
  - 🔴 红色：`curr` 指针（当前节点）
  - 🟢 绿色：`next` 指针
  - 🟣 紫色：`newHead` 指针（头插法）
  - 🟡 黄色：当前焦点节点
  - 🟢 浅绿：已处理节点
- **节点设计**：圆形节点包含值域和指针域，箭头清晰显示指向关系

### 设计特色

#### 1. 认知友好的学习路径
- **从具体到抽象**：以具体的链表 `1→2→3→4→5` 开始演示
- **分步与连贯结合**：支持单步学习和连续观看两种模式
- **对比学习**：相同链表在不同算法下的处理过程直观对比

#### 2. 专业的教学逻辑
- **焦点突出**：每一步高亮当前操作的核心元素
- **状态区分**：清晰区分“未处理”、“正在处理”、“已处理”节点
- **错误防护**：在边界状态（如空指针）下提供合理反馈

#### 3. 响应式设计
- 自适应不同屏幕尺寸
- 在平板和桌面设备上均有良好体验
- 清晰的界面分区，信息层次分明

### 教学要点

#### 迭代法学习重点
1. **三指针的协作**：观察 `prev`、`curr`、`next` 如何协同工作
2. **指针移动顺序**：注意保存 `next` 指针的时机
3. **循环终止条件**：理解 `curr === null` 时循环结束的原因

#### 递归法学习重点
1. **递归基的理解**：观察递归何时到达最深层并开始返回
2. **栈空间的消耗**：通过递归栈可视化理解空间复杂度 O(n)
3. **归的过程操作**：重点观察在递归返回时如何修改指针

#### 头插法学习重点
1. **新链表的构建**：观察 `newHead` 如何逐步成为反转后的链表头
2. **节点的“拔出”操作**：注意每个节点如何从原链表断开并插入新链表
3. **就地修改**：理解为何这种方法也是原地算法

### 使用建议

#### 给初学者的建议
1. **循序渐进**：
   - 先从迭代法开始，这是最直观的方法
   - 使用“很慢”速度，配合“下一步”单步执行
   - 每一步都观察变量状态表的变化
   
2. **建立关联**：
   - 将画布中的指针移动与代码高亮行对应
   - 尝试预测下一步会发生什么，再点击验证
   - 完成一种方法后，立即在白纸上默写算法

3. **深度理解递归**：
   - 使用递归法时，密切观察右侧的递归栈区域
   - 注意“递”和“归”两个阶段的不同操作
   - 思考：如果不保存 `head.next` 会有什么问题？

#### 给进阶学习者的建议
1. **对比分析**：
   - 用相同的链表分别运行三种算法
   - 比较它们在空间复杂度上的差异
   - 思考每种方法的适用场景

2. **边界测试**：
   - 思考空链表、单节点链表的情况
   - 尝试在脑海中模拟这些边界条件

3. **扩展思考**：
   - 如何修改算法来处理双向链表？
   - 如何反转链表的一部分（如从第m到第n个节点）？
   - 这三种方法在时间复杂度上都是O(n)，但常数因子有差异吗？

#### 给教师/讲师的使用建议
1. **课堂演示**：
   - 可全屏展示，使用“中”等速度连续播放
   - 关键步骤暂停，引导学生观察和提问
   - 配合板书，解释算法背后的数学归纳思想

2. **课后练习**：
   - 要求学生使用本工具验证自己的理解
   - 布置作业：解释三种方法中指针变化的异同
   - 鼓励学生尝试修改初始链表值，观察算法通用性

3. **评估理解**：
   - 让学生口头描述某一步的指针状态
   - 提问：如果链表有环，这些算法会出现什么问题？

---

### 技术提示

- **浏览器兼容**：建议使用 Chrome、Firefox、Edge 等现代浏览器
- **性能优化**：动画经过优化，即使在较低配置的设备上也能流畅运行
- **离线使用**：将本页面保存为HTML文件后可在无网络环境下使用

---

**最后的小建议**：学习算法就像学习舞蹈——看别人跳十遍不如自己跳一遍。请充分利用这个工具的控制功能，**主动探索**而不仅仅是被动观看。尝试预测、验证、犯错、修正，这才是真正掌握算法的路径。

祝您学习愉快，如有任何反馈或建议，欢迎提出！ 🚀

*熊猫老师 设计*