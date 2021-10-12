---
layout: default
---

<!--  <h1 align='center'><font size='10'> TOWARDS HIGH-FIDELITY SINGING VOICE CONVERSION WITH ACOUSTICREFERENCE AND CONTRASTIVE PREDICTIVE CODING </font></h1> -->

Paper: [arxiv](https://arxiv.org/abs/2110.04754)

# Abstract

Recently, phonetic posteriorgrams (PPGs) based methods have been quite popular in non-parallel singing voice conversion systems. However, due to the lack of acoustic information in PPGs,  style and naturalness of the converted singing voices are still limited. To
solve these problems, in this paper, we utilize an acoustic reference encoder to implicitly model singing characteristics. We experiment with different auxiliary features, including mel spectrograms, HuBERT, and the middle hidden feature (PPG-Mid) of pretrained automatic speech recognition (ASR) model, as the input of the reference encoder, and finally find the HuBERT feature is the best choice. In addition, we use contrastive predictive coding (CPC) module to further smooth the voices by predicting future observations in latent space. Experiments show that, comparing with the baseline models, our proposed model can significantly improve the naturalness of converted singing voices and the similarity with the target singer. Moreover, our proposed model can also make the speakers with just speech data sing. 

# Audio Samples

## Source Samples

2 female singing audio and 2 male singing audio are presented as the source samples. The samples are from different singers.

| | Samples |
| --- | --- |
| F1 | <audio id="audio" controls="" preload="none" style="height: 40px"> <source id="wav" src="audiofile/source_data/female_05_37.wav"></audio> |
| F2 | <audio id="audio" controls="" preload="none" style="height: 40px"> <source id="wav" src="audiofile/source_data/female_05_3.wav"></audio> |
| M1 | <audio id="audio" controls="" preload="none" style="height: 40px"> <source id="wav" src="audiofile/source_data/male_13_2.wav"></audio> |
| M2 | <audio id="audio" controls="" preload="none" style="height: 40px"> <source id="wav" src="audiofile/source_data/male_05_30.wav"></audio> |

## In Domain Singing Voice Conversion

### Target Singers
The following audio samples are from the target female and male singers from NUS-48E singing corpus.

| Target | Samples |
|  ----  | ----  |
| Female | <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audiofile/targe_timbre/female.wav"></audio> |
| Male | <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audiofile/targe_timbre/male.wav"></audio> |

### Converted Samples

#### Target Female

| | F1 | F2 | M1 | M2 |
| --- | --- | --- | --- | --- |
| Baseline1 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_f2f_NJAT_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_f2f_NJAT_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_m2f_NJAT_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_m2f_NJAT_05_30.wav"></audio> |
| Baseline2 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_f2f_NJAT_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_f2f_NJAT_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_m2f_NJAT_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_m2f_NJAT_05_30.wav"></audio> |
| Prop_mel | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_f2f_NJAT_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_f2f_NJAT_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_m2f_NJAT_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_m2f_NJAT_05_30.wav"></audio> |
| Prop_ppg-mid | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_f2f_NJAT_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_f2f_NJAT_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_m2f_NJAT_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_m2f_NJAT_05_30.wav"></audio> |
| Prop_hub | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_f2f_NJAT_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_f2f_NJAT_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_m2f_NJAT_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_m2f_NJAT_05_30.wav"></audio> |
| **Prop_hub_cpc** | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_f2f_NJAT_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_f2f_NJAT_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_m2f_NJAT_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_m2f_NJAT_05_30.wav"></audio> |

#### Target male

| | F1 | F2 | M1 | M2 |
| --- | --- | --- | --- | --- |
| Baseline1 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_f2m_VKOW_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_f2m_VKOW_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_m2m_VKOW_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline1_m2m_VKOW_05_30.wav"></audio> |
| Baseline2 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_f2m_VKOW_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_f2m_VKOW_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_m2m_VKOW_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/baseline2_m2m_VKOW_05_30.wav"></audio> |
| Prop_mel | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_f2m_VKOW_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_f2m_VKOW_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_m2m_VKOW_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/mel_m2m_VKOW_05_30.wav"></audio> |
| Prop_ppg-mid | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_f2m_VKOW_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_f2m_VKOW_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_m2m_VKOW_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/ppg30_m2m_VKOW_05_30.wav"></audio> |
| Prop_hub | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_f2m_VKOW_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_f2m_VKOW_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_m2m_VKOW_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubert_m2m_VKOW_05_30.wav"></audio> |
| **Prop_hub_cpc** | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_f2m_VKOW_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_f2m_VKOW_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_m2m_VKOW_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/in_domain_converted/hubertcpc_m2m_VKOW_05_30.wav"></audio> |

## Cross Domain Singing Voice Conversion

### Target Speakers
The following audio samples are from the target female and male speakers from VCTK speech corpus.

| Target | Samples |
|  ----  | ----  |
| Female | <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audiofile/targe_timbre/vctktts228_EN_00014.wav"></audio> |
| Male | <audio id="audio" controls="" preload="none" style="width: 250px;"> <source id="wav" src="audiofile/targe_timbre/vctktts227_EN_00029.wav"></audio> |

### Converted Samples

#### Target Female

| | F1 | F2 | M1 | M2 |
| --- | --- | --- | --- | --- |
| Baseline1 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_f2f_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_f2f_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_m2f_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_m2f_05_30.wav"></audio> |
| Baseline2 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_f2f_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_f2f_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_m2f_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_m2f_05_30.wav"></audio> |
| **Prop_hub_cpc** | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_f2f_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_f2f_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_m2f_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_m2f_05_30.wav"></audio> |

#### Target male

| | F1 | F2 | M1 | M2 |
| --- | --- | --- | --- | --- |
| Baseline1 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_f2m_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_f2m_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_m2m_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline1_m2m_05_30.wav"></audio> |
| Baseline2 | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_f2m_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_f2m_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_m2m_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/baseline2_m2m_05_30.wav"></audio> |
| **Prop_hub_cpc** | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_f2m_05_37.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_f2m_05_3.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_m2m_13_2.wav"></audio> | <audio id="audio" controls="" preload="none" style="width: 140px;height: 50px"> <source id="wav" src="audiofile/cross_domain_converted/hubertcpc_m2m_05_30.wav"></audio> |

