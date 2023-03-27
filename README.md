# Quad-GAN

###An implementation of Generative Adversarial Networks for Joint Distribution Matching. Built on top of Triangle GAN (https://arxiv.org/abs/1709.06548).

The essence of a \(\Delta\) GAN is that it is able to do a bi-directional mapping between two random variables \((x, y)\) from two domains by matching the three joint distributions of  \(p(x,y), p_x(\Tilde{x},y), p_y(x,\Tilde{y})\) where \(p(\Tilde{x}|y)\) and \(p(\Tilde{y}|x))\) represent the generated conditional distributions.
\newline
We can take this one step ahead and attempt to a generate directional mappings between three random variables by having two real-domain random variables generate the third conditional variable i.e \((x,y) \xrightarrow{} \Tilde{z}\), \((y,z) \xrightarrow{} \Tilde{x}\) and \((x,z) \xrightarrow{} \Tilde{y} \). The joint distributions under consideration will be \(p(x,y,z)\), \(p(\Tilde{x},y,z)\), \(p(x,\Tilde{y},z)\), \(p(x,y,\Tilde{z})\). Since we are matching 4 joint distributions, it is called a Quad GAN.
