---
layout: default
---

 <h1 align='center'><font size='10'> TOWARDS HIGH-FIDELITY SINGING VOICE CONVERSION WITH ACOUSTICREFERENCE AND CONTRASTIVE PREDICTIVE CODING </font></h1>

Paper: [arxiv](https://arxiv.org/abs/2010.14804)

# Abstract

Recently, phonetic posteriorgrams (PPGs) based methods have been quite popular in non-parallel singing voice conversion systems. However, due to the lack of acoustic information in PPGs,  style and naturalness of the converted singing voices are still limited. To
solve these problems, in this paper, we utilize an acoustic reference encoder to implicitly model singing characteristics. We experiment with different auxiliary features, including mel spectrograms, HuBERT, and the middle hidden feature (PPG-Mid) of pretrained automatic speech recognition (ASR) model, as the input of the reference encoder, and finally find the HuBERT feature is the best choice. In addition, we use contrastive predictive coding (CPC) module to further smooth the voices by predicting future observations in latent space. Experiments show that, comparing with the baseline models, our proposed model can significantly improve the naturalness of converted singing voices and the similarity with the target singer. Moreover, our proposed model can also make the speakers with just speech data sing. 

# Audio Samples
## Target Singers

The following audio samples are from the target female and male singers.

| Target | Samples |
|  ----  | ----  |
| Female | <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audios/BB/gt/BB006F24I016.wav"></audio> <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audios/BB/gt/BB009F24I024.wav"></audio> |
| Male | <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audios/AM2/gt/0003_048-03.wav"></audio> <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audios/AM2/gt/0006_041-08.wav"></audio> |

