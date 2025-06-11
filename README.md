<!-- PROJECT LOGO -->
<br />

<h3 align="center">CreatiPoster: Towards Editable and Controllable<br>Multi-Layer Graphic Design Generation</h3>
<p align="center">
  <a href="https://zhaozhang.net/">Zhao Zhang</a>, Yutao Cheng, Dexiang Hong, <a href="https://dblp.org/pid/210/5108.html">Maoke Yang</a>,<br>
  Gonglei Shi, Lei Ma, Hui Zhang, Jie Shao, and Xinglong Wu<br>
  <a href="#"><strong>[arXiv 📚]</strong></a> 
  <a href="#"><strong>[Model ⚙️]</strong></a> 
  <a href="#"><strong>[Results 🖼️]</strong></a> 
  <a href="#bib"><strong>[Bibtex 🔗]</strong></a>
</p>


***
This repository open-sources CreatiPoster, an AI-driven graphic design generation system that supports multi-layer and editable compositions with strong visual appeal.

<p align="center"> <img src=".repo/teaser.jpg" alt="teaser"/></p>

Example of editing a graphic composition in the CreatiPoster editor. Users can modify text, assets, layout, and style through an intuitive GUI with JSON field controls, enabling professional-level customization.
<p align="center"> <img src=".repo/editing.png" alt="editing" width="300" /></p>




## News
[2024/06/13] Our manuscript is now available on <a href="#">arXiv</a>.

## To-Do List
- [ ] Release the training/inference code
- [ ] Release the CreatiPoster-F checkpoint.
- [ ] Release training dataset and eval set.


## Method
Overview of the CreatiPoster pipeline: User inputs are processed by the protocol model to generate editable design layers, while the background model creates a complementary background. The final graphic composition integrates both outputs seamlessly.

![pipeline](.repo/pipeline.png)


## Show Cases

### Different interaction modes
CreatiPoster supports diverse interaction modes, including prompt-only, asset-only, mixed input, and explicit specification of text/asset layout or attributes.

![modes](.repo/interaction.png)

### Animated poster
CreatiPoster can extend static graphic compositions to animated posters. Videos are generated from background layers using an image-to-video model.

<img src=".repo/man.gif" alt="animated" style="width:37%; margin:5px;">
<img src=".repo/sheep.gif" alt="animated" style="width:27.5%; margin:5px;">
<img src=".repo/snow.gif" alt="animated" style="width:27.8%; margin:5px;">
<img src=".repo/sea.gif" alt="animated" style="width:14%; margin:8px;">
<img src=".repo/cherry.gif" alt="animated" style="width:24.7%; margin:8px;">
<img src=".repo/cat.gif" alt="animated" style="width:33%; margin:8px;">
<img src=".repo/face.gif" alt="animated" style="width:13.9%; margin:8px;">

### Multilingual poster
CreatiPoster's multilingual capabilities: Despite training data only including Simplified Chinese and English graphic compositions, pre-training and multilingual fine-tuning enable the protocol model to generalize to other languages.

![multilingual](.repo/multilingual.png)

### Text overlay
Our protocol model enables direct text overlay on uploaded assets without needing the background model. This is ideal for tasks like adding titles to e-commerce product images or text overlays on social media photos.

![overlay](.repo/overlaying.png)

### Poster re-layout
Given an original graphic design, CreatiPoster generates alternative layouts of various sizes while preserving content and style. By reusing rendered layers and predicting new foreground/background elements, this approach enables efficient adaptation of designs for different platforms.

![relayout](.repo/relayout.png)



## Application
This system has been integrated into [Pippit AI](http://pippit.capcut.com) to power its poster generation capabilities. 

![Pippit](.repo/pippit_f2d.gif)



