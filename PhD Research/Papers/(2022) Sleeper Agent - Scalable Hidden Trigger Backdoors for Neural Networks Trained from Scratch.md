#sleeperagent #backdoor #datapoisoning #gradientmatching #gradientalignment
# <font color="#00b0f0">Key Notes</font>
- Backdoor attack using data poisoning approach
- The main technique: gradient matching (a.k.a gradient alignment)
- This is an extension of the **Witches' Brew**

# <font color="#00b0f0">Method</font>

## <font color="#00b050">Notation</font>

$t$: trigger
$p$: perturbation
$y_t$: the target label
$x_s$: a sample from the source class
$x_t$: a sample from the target class

## <font color="#00b050">Description</font>

- If we could, we would add the trigger to the images of the source class, and change their labels to the target class. 
- However, the mismatch between labels and images would reveal the attack. 
- Instead, we perturb some of the training images in a way that they have a similar effect in the training process.

$$g_1 = \nabla l_\theta(f(x_s\oplus t),y_t)$$
$$g_2=\nabla l_\theta(f(x_t+p), y_t)$$
- Minimize 
$$1-\dfrac{<g_1,g_2>}{||g_1|| ||g_2||}$$
