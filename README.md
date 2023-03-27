# Quad-GAN

### An implementation of Generative Adversarial Networks for Joint Distribution Matching. Built on top of Triangle GAN (https://arxiv.org/abs/1709.06548).

The essence of a $\Delta$ GAN is that it is able to do a bi-directional mapping between two random variables \((x, y)\) from two domains by matching the three joint distributions of  $p(x,y), p_x(\tilde{x},y), p_y(x,\tilde{y})$ where $p(\tilde{x}|y)$ and $p(\tilde{y}|x))$ represent the generated conditional distributions.
\newline
We can take this one step ahead and attempt to a generate directional mappings between three random variables by having two real-domain random variables generate the third conditional variable i.e $(x,y) \xrightarrow{} \tilde{z}$, $(y,z) \xrightarrow{} \tilde{x}$ and $(x,z) \xrightarrow{} \tilde{y} $. The joint distributions under consideration will be $p(x,y,z)$, $p(\tilde{x},y,z)$, $p(x,\tilde{y},z)$, $p(x,y,\tilde{z})$. Since we are matching 4 joint distributions, it is called a Quad GAN.
