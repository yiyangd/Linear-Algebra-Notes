## Linear Algebra Note 01: Vectors
> 此篇笔记是**线性代数笔记**系列第1篇笔记，记录了**3Blue1Brown**的**Essence of linear algebra**系列课程的第1章内容，即线性代数中最最基础的概念 —— **向量(Vectors)**, 并讨论了**向量相加(Vector Addition)** 和 **向量放缩(Vector Scaling)**, 并强调它们在线性代数中的重要性。

![](https://github.com/yiyangd/Linear-Algebra-Notes/blob/main/Linear-Algebra-Note-01-Vectors/gif/LA0100.gif)


The **fundamental root of a tall building block for linear algebra** is the **vector**.   
**线性代数中最基础的组成部分**就是**向量**
- think about **an arrow inside a coordinate system** with **its tail sitting at the origin**.  
**考虑一个箭头，在某个坐标系中**，并且**箭头起点位于原点**。
### 1. Vectors in 2D Plane


![](https://github.com/yiyangd/Linear-Algebra-Notes/blob/main/Linear-Algebra-Note-01-Vectors/gif/LA0101.gif)

**The coordinates  of a vector in 2D plane is a pair of numbers** that basically give instructions for how to get **from the tail** of that vector—at the origin—**to its tip**.  
**在2D平面中一个向量的坐标由一对数构成**，这对数指导你如何**从原点**（向量起点）出发**到达它的尖端**（向量终点）
- The **first number** tells you **how far to walk along the x-axis**—positive numbers indicating rightward motion, negative numbers indicating leftward motion  
**第一个数**告诉你**沿着x轴走多远**，正数代表向右移动，负数代表向左移动
- and **the second number** tell you **how far to walk parallel to the y-axis** after that—positive numbers indicating upward motion, and negative numbers indicating downward motion.  
**第二个数**告诉你在此之后**沿着平行y轴的方向走多远**，正数代表向上移动，负数代表向下移动
- **Every pair of numbers** gives you **ONE and ONLY ONE vector**, and **every vector** is associated with **ONE and ONLY ONE** pair of numbers.  
**每一对数**给出**唯一一个向量**而**每一个向量**恰好对应**唯一的一对数**
### 2. Vectors in 3D Space
![](https://files.mdnice.com/user/1474/1456d43d-fe15-4110-8aff-8f554fa0d5af.gif)

**In three dimensions** we **add a third axis, called the z-axis**, which **is perpendicular to both the x and y-axes**, and in this case each vector is associated with an **ordered triplet of numbers**:     
**在三维空间中**我们**需要添加垂直于x轴和y轴的第三根轴 - z轴**，这种情况下，每个向量就与一个**有序三元数组**对应：
- **each number tells us how far to move** along/parallel to the x,y and z-axis,     
**每个数告诉我们**沿着/平行于x,y和z轴**走多远**,
- **every triplet of numbers** gives you **one unique vector in 3D space**, and **every vector in 3D space** gives you **exactly one triplet of numbers**.    
**每一个三元数组**给出**唯一一个三维空间的向量**，而**每一个三维空间的向量**恰好对应**唯一一个三元数组**

### 3. Vector Addition
![](https://files.mdnice.com/user/1474/e8df330b-f5be-41e3-b8a7-e4e133e10de3.gif)

One way to think about **Vector Addition** is that **each vector represents a certain movement**— **a step** with a **certain distance** and **direction** in space.
一种思考**向量加法**的方法是**把每个向量看作一种特定的运动**，即在空间中**朝着某个方向迈出一定距离**

![](https://files.mdnice.com/user/1474/77a30ebf-da69-4aef-bb6d-46612cabe71d.gif)

For examples, **the first vector here has coordinates (1,2)**, and **the second one has coordinates (3,-1)**.  
举个例子，**第一个向量的坐标是(1, 2)**, **第二个向量的坐标是(3,-1)**
- when you **take the vector sum using this tip-to-tail method,** you can think of a **four-step path** from the origin to the tip of the second vector:   
当你**用向量首尾连接的方法加和向量时**,你可以把它看做一个从原点出发，到第二个向量终点的**四步运动:**
  - **walk 1 to the right, then 2 up, then 3 to the right, then 1 down.**  
**向右1步，向上2步，向右3步，最后向下1步**

![](https://files.mdnice.com/user/1474/fd783c3c-fa73-4b1b-b6dd-7338c3e5f712.gif)

**Re-organising these step**s so that you **first do all of the rightward motion**, **then do all of the vertical motion:**  
我们**重新编排它们的顺序**，使得我们**先完成所有水平运动**，**再完成所有竖直运动:**
- first move `1+3` to the right, then move `2+(-1)` up   
你可以看出来，首先向右`(1+3)`步，然后向上`2+(-1)`步
- so the new vector has coordinates `1+3` and `2+(-1)`   
所以新向量的坐标就是`(1+3, 2+(-1))`
- in general, **vector addition** is **matching up their terms, and adding each one of those components together**.  
总的来说，**向量加法**就是**把向量中对应项相加**
$$
\begin{bmatrix}
x_1 \\
y_1 
\end{bmatrix}
+
\begin{bmatrix}
x_2\\
y_2
\end{bmatrix}
= 
\begin{bmatrix}
x_1+x_2\\
y_1+y_2
\end{bmatrix}
$$

### 4. Vector Scaling
![](https://files.mdnice.com/user/1474/c025ed70-e22c-4a13-bcf0-8c5b38349951.gif)

If we take the number `2`, and **multiply it by a given vector**, it means we **stretch out that vector so that it's 2 times as long as the original vector**.  
比如说我们选择数字2，**它与一个给定向量相乘**, 意味着**把这个向量拉长为原向量的2倍**
- **multiply that vector by 1/3**, it means we **squish it down so that it's 1/3 of the original length**.    
**将向量乘以1/3**，就意味着**这个向量长度缩短为原来的1/3**
- **multiply it by a negative number, like -1.8**, then **the vector first gets flipped around**, then **stretched out by that factor of 1.8**.  
当向量与一个负数相乘时，比如-1.8, 说明**这个向量首先反向**，然后**伸长为原来的1.8倍**
- throughout linear algebra, **one of the main things that numbers do is scale vectors**, so it's common to use the word **scalar** pretty much **interchangeably** with the word **number**.  
实际上自始至终，**数字在线性代数中起到的主要作用就是缩放向量**, 所以**标量**和**数字**两个词通常在这里**可以相互替换**

![](https://files.mdnice.com/user/1474/a6972bd2-3580-4306-a3af-d37a07745a4a.gif)

**Stretching out a vector by a factor of 2**, corresponds to **multiplying each of its components by that factor, 2**, 
**将一个向量伸长为原来的2倍**,对应于**将每一个分量分别乘以2**
- in general, **multiplying a given vector by a scalar s** means **multiplying each one of those components by that scalar s**.     
总的来说，**向量与标量s相乘**就是**将向量中的每个分量与标量s相乘**

$$
s
\cdot
\begin{bmatrix}
x\\
y
\end{bmatrix}
= 
\begin{bmatrix}
s \cdot x\\
s \cdot y
\end{bmatrix}
$$
> **要点:**
> - 🎯 **向量**可以被视为**空间中的箭头**、**有序的数字列表**或**一般的数学对象**。
> - 🎯 **向量相加**涉及将一个向量移动，使其尾部与另一个向量的顶部对齐，从而得到它们的和。
> - 🎯 **向量放缩**通过标量对向量进行缩放，拉伸或收缩其长度，并可能反转其方向。


### Resources"
[1] https://youtu.be/fNk_zzaMoSs
