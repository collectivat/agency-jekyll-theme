---
layout: asr_base
ref: asr
lang: en
permalink: asr
---
<style>
table {
    width:100%;
}
</style>

# Resources for Speech Technologies

As a part of our mission we provide open data and resources to the public concerning speech technologies. You can find a detailed list here with short explanations and further references to get more information. Also, please visit our [wiki][wiki] for more details on speech technologies and the models we maintain.
  
<br/> 

| Name                                    | Language | Type           | License       | Download     |
|---------------------------------------  | -------- | -----------    | --------      | ------------ |
| [TV3Parla][2]                      v0.3 | Catalan  | acoustic model | GNU AGPL-3.0  | [link][M0.3] |
| [TV3Parla+ParlamentParla][2]       v0.2 | Catalan  | acoustic model | GNU AGPL-3.0  | [link][M0.4] |
| [TV3Parla Corpus][1]               v0.3 | Catalan  | audio corpus   | CC-BY-NC 4.0  | [link][Ctv3] |
| [ParlamentParla Corpus - clean][1] v1.0 | Catalan  | audio corpus   |  CC-BY 4.0    | [link][CpC]  |
| [ParlamentParla Corpus - other][1] v1.0 | Catalan  | audio corpus   |  CC-BY 4.0    | [link][CpO]  |
| [ParlamentParla Corpus - old][1]   v0.3 | Catalan  | audio corpus   |  CC-BY 4.0    | [link][Cp0.3]|
| OpenSubtitles LM                   v1.0 | Catalan  | language model |  CC-BY 4.0    | [link][LMos] |
 
<br/>
<br/>

## Acoustic corpora

For the two projects we finished successfully, we have gathered publicly available speech data and converted them into acoustic training corpora. These data sets are available for download with varying open licenses.

* **TV3Parla**

  This corpus includes 240 hours of Catalan speech from broadcast material. The details of segmentation, data processing and also model training are explained in [Külebi, Öktem; 2018](https://www.isca-speech.org/archive/IberSPEECH_2018/abstracts/IberS18_P1-2_Kulebi.html). The content is owned by Corporació Catalana de Mitjans Audiovisuals, SA (CCMA); we processed their material and hereby making it available under their [terms of use](http://www.ccma.cat/avis-legal/condicions-utilitzacio-del-portal/).


  The corpus can be reached [here][Ctv3] under a [CC BY-NC 4.0][ccbync] license.  

  You can cite the data using the BibTeX entry:
  ```
  @inproceedings{Külebi2018,
    author={Baybars Külebi and Alp Öktem},
    title={Building an Open Source Automatic Speech Recognition System for Catalan},
    year=2018,
    booktitle={Proc. IberSPEECH 2018},
    pages={25--29},
    doi={10.21437/IberSPEECH.2018-6},
    url={http://dx.doi.org/10.21437/IberSPEECH.2018-6}
  }
  ```
  <br/>

  This project was supported by the [Softcatalà Association](https://www.softcatala.org/).

* **ParlamentParla**

  We have gathered this audio corpus from the recordings and the transcripts of the Catalan Parliament ([Parlament de Catalunya](https://www.parlament.cat/)) plenary sessions. We have aligned the transcriptions with the recordings and extracted the cleanest 320 hours to train speech models. The content belongs to the Catalan Parliament and the data is released conforming their [terms of use](https://www.parlament.cat/pcat/serveis-parlament/avis-legal/).

  As of version 1.0, the corpus can be reached in two parts; 90 hours of [clean][CpC] and 230 hours of [other][CpO] quality segments, both under a [CC BY 4.0][ccby] license. In addition to the segmented audio files and the transcriptions, the [v0.3 corpus][Cp0.3] also includes per intervention full text vs audio links. In the near future we will also publish the structured form of the parliamentary sessions (session id, speaker, intervention text, intervention duration etc.).  
  <br/>

  This project was supported by the [Department of Culture](http://cultura.gencat.cat/) of the Catalan autonomous government.

## ASR models

These are the ASR models that we trained, using the aforementioned corpora. For now we used the [CMUSphinx](https://cmusphinx.github.io/) speech recognition toolkit, that is the result of over 20 years of research in Carnegie Mellon University. Although currently the state-of-the-art is hybrid Hidden Markov Model (HMM) and Neural Networks (NN) technologies such as Kaldi, `pocketsphinx` tool is still the leader in offline decoding for resource limited environments such as hand-held devices. We continue our work on maintaining and bettering the models in our [repository](https://github.com/collectivat/cmusphinx-models). You can find installation and configuration guides, including tutorials on basic use-cases in the [wiki][wiki].

Here is a list of latest CMUSphinx models:

* [TV3Parla v0.3][M0.3]: `sphinxtrain` 5pre-alpha continuous model
* [TV3Parla+ParlamentParla v0.2][M0.4]: `sphinxtrain` 5pre-alpha continuous model
  <br/>  
  <br/> 
  <br/>

The preparation of this page was supported by the [Culture Department](http://cultura.gencat.cat/) of the Catalan autonomous government.

<img src="/img/logo_generalitat.png" width="400"/>

[wiki]: https://github.com/collectivat/cmusphinx-models/wiki
[ccby]: https://creativecommons.org/licenses/by/4.0/
[ccbync]: https://creativecommons.org/licenses/by-nc/4.0/
[gapgl]: https://www.gnu.org/licenses/agpl-3.0.html
[Ctv3]: http://laklak.eu/share/tv3_0.3.tar.gz
[CpC]: http://laklak.eu/share/parlament_v1.0_clean.tar.gz
[CpO]: http://laklak.eu/share/parlament_v1.0_other.tar.gz
[Cp0.3]: http://laklak.eu/share/parlament_0.2.tar.gz
[M0.3]: https://cloud.laklak.eu/s/MY0SYpTap8w0WuK
[M0.4]: https://cloud.laklak.eu/s/4o2b5MrHckMYCXo
[LMos]: https://cloud.laklak.eu/s/zY7J2jGD8Hgnzpj
[LMvq]: https://cloud.laklak.eu/s/dXCsjqSfjk6Eo7R
[2]: #asr-models
[1]: #acoustic-corpora
