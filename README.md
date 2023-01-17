## OpenGVLab

> Opensource general vision AI ecosystem by Shanghai AI Lab

### Why general vision AI

In last decade, AI technology, along with its applications, have witnessed rapid growth, fueled by more data, compute power, and better algorithms, deep learning algorithms especially. AI even surpass human level skills in many tasks such as facial recognition, poker, and go. However, current AI models are heavily reliant on labeled data, and require different models for different tasks. It’s imperative to make AI models more generalized in order to lower AI development costs. More specifically, future vision models will show greater ability to generalize in terms of tasks, context, modality, and exhibit deeper levels of cognition. As vision is a key component of AI models, we believe generalized vision models will be the next big step for AI. With general vision models, we hope to empower hundreds of business sectors more cost effectively and achieve more sustainable AI developmentm and will lead to the next breakthroughs in AGI, artificial general intelligence.

### Our work

During the World Artificial Intelligence Conference in September 2022, we released INTERN 2.0, consisting of 3 general models for image, video, and translation tasks respectively. Each of these general models have made significant improvements over existing work in their modality.
- The general image model, which is based upon dynamic sparse convolutions, can adapt to different convolution location and combination configurations based on different visual tasks, optimizing for the task at hand. The general image model, together with the general video model, jointly reached SOTA performance in 50 visual tasks covering 12 categories.
- The general video model utilizes a combination of masked signal learning and contrastive learning to break the bottleneck related to self-supervised training, creating for the first time a systematic, dynamical, and perceptual large video model. This video model covers the three core areas of video recognition, video perception, and temporal semantic analysis, achieving SOTA performance with over 90% top1 accuracy on the Kinetics 400 main video benchmark.
- The general translation model currently supports up to 400 languages. Utilizing 1.3 billion model parameters, the general translation model reaches SOTA performance in open-source translation models by a large margin.

> General image model benchmarks

<img width="75%" src="assets/images/general-image-pk.png" style="display:block;margin-left:auto;margin-right:auto">

> General video model benchmarks

<img width="90%" src="assets/images/general-video-pk.png" style="display:block;margin-left:auto;margin-right:auto">

<br>

> Overview of the general image model: InternImage

<video width="100%" controls>
  <source src="https://user-images.githubusercontent.com/94522163/211799801-cf9bb31b-fa4a-46f8-9edb-1873e445ab29.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

> Overview of the general video model: InternVideo

<video width="100%" controls>
  <source src="https://user-images.githubusercontent.com/94522163/211804947-582c52d7-e426-41e1-926f-2b821a5c844f.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
