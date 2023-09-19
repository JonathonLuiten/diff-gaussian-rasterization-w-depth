
This is a clone of https://github.com/graphdeco-inria/diff-gaussian-rasterization/tree/59f5f77e3ddbac3ed9db93ec2cfe99ed6c5d121d

However, it has been edited by Jonathon Luiten to also render 'depth' as well as colour.

This is needed for Jonathon's Dynamic 3D Gaussians work which can be found here: http://dynamic3dgaussians.github.io

By default, the depth is calculated as 'mean depth', but there is commented out code which also calculates 'median depth' if preferred.

Note that the backward pass for the depth has not been implemented, so it won't work for training with depth ground-truth.

Note that the code in this repo follows the (non commercial) license of Inria as laid out in LICENSE.md

If you're using this as part of the Dynamic Gaussian code, just follow the installation instruction for that codebase.

To install this stand-alone I have been doing the following (although I don't think this is necessarily the best way):
```
git clone git@github.com:git@github.com:JonathonLuiten/diff-gaussian-rasterization-w-depth.git
cd diff-gaussian-rasterization-w-depth
python setup.py install
pip install .
```

Original readme below:

# Differential Gaussian Rasterization

Used as the rasterization engine for the paper "3D Gaussian Splatting for Real-Time Rendering of Radiance Fields". If you can make use of it in your own research, please be so kind to cite us.

<section class="section" id="BibTeX">
  <div class="container is-max-desktop content">
    <h2 class="title">BibTeX</h2>
    <pre><code>@Article{kerbl3Dgaussians,
      author       = {Kerbl, Bernhard and Kopanas, Georgios and Leimk{\"u}hler, Thomas and Drettakis, George},
      title        = {3D Gaussian Splatting for Real-Time Radiance Field Rendering},
      journal      = {ACM Transactions on Graphics},
      number       = {4},
      volume       = {42},
      month        = {July},
      year         = {2023},
      url          = {https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/}
}</code></pre>
  </div>
</section>