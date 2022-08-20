
## Project

The widespread use of devices with internet access, together with the increasing availability of cloud computing platforms and recent advances in AI, has given rise to a multitude of Machine Learning as a Service applications. With their increasing popularity has also come increasing awareness that they also potentially compromise users' privacy, as shown by the intense public debate that led to, and followed, the creation of GDPR (EU’s General Data Protection Regulation). Among other data types, speech stands out by the amount of information that may be extracted from it which goes far beyond the linguistic contents. In fact, one can extract information regarding demographic traits such as gender, age range, accent, level of education, physical characteristics such as height, emotional status, personality traits, levels of stress, intoxication, sleepiness, etc. Moreover, speech can be used as a biomarker for many diseases that affect speech. This implies that one should regard speech as “Personally Identifiable Information”. Privacy-preserving machine learning for speech is thus the overarching topic of the PRIVADIA project.

Among many other tasks, current machine learning models are able to automatically transcribe speech recordings, identify speakers, and perform "diarization", often referred to as the problem of determining “who spoke when” in a conversation. Privacy in diarization is the particular focus of the current project, as illustrative of a very complex processing chain, related with speaker characteristics. This project addresses this topic by combining state-of-the-art diarization methods (typically based on speaker embeddings obtained from the hidden layers of deep neural networks) with cryptographic techniques.

The first task of the project consisted of implementing a baseline approach, without privacy concerns. Several baselines were explored, using increasingly complex models, in an effort to reach a good privacy/computational and communication costs/quality trade-off. Specifically, the first baseline we explored was based on Hierarchical Clustering using the Bayesian Information Criterion; the second was based on Binary Keys; finally, the third replicated the DIHARD III challenge baseline. The latter is based on template speaker representations, a.k.a. speaker embeddings. Concretely, it uses x-vectors - the current state-of-the-art in terms of speaker representations – combined with Agglomerative Hierarchical Clustering and Variational Bayes – Hidden Markov Model (VB-HMM)-based re-segmentation. This system obtained the best diarization results when evaluated over the multiple domains of the dataset distributed for the DIHARD III challenge, using the same scoring procedure as the challenge. 

We also explored a variation of this baseline, using i-vectors - one of the most popular speaker representations, proposed in 2009. With this system, we obtained an acceptable degradation of 2 − 3% relative to the x-vector system. The fact that the i-vector extraction process requires a much lower number of non-linear operations when compared to x-vectors provided the motivation for developing a privacy-preserving version of this simpler system, as it allowed us to use Homomorphic Encryption (HE), one of the most secure cryptographic techniques for shared computations, which has several limitations regarding the computation of non-linear operations. However, during the development of this solution, we determined that a privacy-preserving implementation of the i-vector extractor using only HE is infeasible. Our next step was thus the development of a privacy-preserving x-vector extractor, using Secure Multiparty Computation (SMC). This helped to solve the computational challenges raised by HE, at the cost of a relaxation of our security model. 
Finally, to have a complete diarization pipeline, we also implemented the Agglomerative Hierarchical Clustering stage in a privacy-preserving way, using vectors transformed with Secure Modular Hashing. Overall, our final system obtains an absolute degradation of ~6% with regard to the baseline, which we consider a reasonable trade-off with privacy.

Given the current relevance of speaker embeddings for other speech processing tasks, the contributions of this project in terms of the privacy-preserving extraction of such embeddings extend beyond diarization. In fact, they may be particularly relevant for automatic speaker verification, allowing users to authenticate themselves without risking the privacy of their voice, while at the same time protecting the service-provider’s model. This is an improvement over current privacy-preserving methods, which assume that speaker embeddings used for authentication are extracted locally by the user. In this project, we showed how speaker embeddings can be extracted while keeping both the speaker’s voice and the service provider’s model private, using SMC. 

In parallel, we also addressed another type of paradigm to avoid the abovementioned computational burden. We showed that it is possible to perturb speech such that a human does not realise it, and such that this perturbation is enough to fool a speaker identification system. In this steganography-inspired method, we generated adversarial examples against speaker identification, by training a Gated Convolutional Autoencoder using a new perceptually motivated multi-objective loss. This work was done in cooperation between the CMU-Portugal team and researchers from the Queen Mary University of London.

## Publications & Presentations

Publications in international conferences:
1.	Shamsabadi, A, Teixeira, F., Abad, A., Raj, B., Cavallaro, A., & Trancoso, I. (2021), Foolhd: Fooling speaker identification by highly imperceptible adversarial disturbances. IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), pp. 6159–6163. doi: 10.1109/ICASSP39728.2021.9413760
(The two first authors contributed equally to this work.)
https://ieeexplore.ieee.org/document/9413760
2.	Ablimit, A., Botelho, C., Abad, A., Schultz, T., & Trancoso, I. (2022). Exploring dementia detection from speech: cross corpus analysis, IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), pp. 6472-6476, doi: 10.1109/ICASSP43922.2022.9747167.
https://ieeexplore.ieee.org/document/9747167
(The two first authors contributed equally to this work.)
3.	Teixeira, F., Abad, A., Raj, B., & Trancoso, I. (2022), Towards End-to-End Private Automatic Speaker Recognition. 23rd Annual Conference of the International Speech Communication Association (Interspeech). 
https://arxiv.org/abs/2206.11750

Book chapters:
1.	Teixeira, F., Abad, A., Trancoso, I., & Raj, B. (2021), Voice Biometrics: Privacy in Paralinguistic and Extra-Linguistic Tasks,” in Voice Biometrics: Technology, trust and security, C. Garcia-Mateo and G. Chollet, Eds. IET, ch. 4, ISBN: 978-1-78561-900-7. 
2.	Trancoso, I. (2021), A Fala como PII (Personally Identifiable Information), in Política do Medo Ou o mundo de hoje entre a privacidade e a segurança. Universidade Católica Editora, ISBN: 9789725408032.
3.	Trancoso, I. Teixeira, F. , Botelho, C. and Abad A. (2022), Treating Speech as Personable Identifiable Information -- Impact in Machine Translation, in Towards Responsible Machine Translation -- Ethical and Legal Considerations in Machine Translation, Helena Moniz & Carla Parra Escartín (eds.), ISBN: 978-3-031-14688-6.

Keynote presentations at international conferences:
1.	Trancoso, I. (2021), Speech as Personally Identifiable Information. Keynote talk at 11th Conference on Speech Technology and Human-Computer Dialogue (SPED 2021), Bucharest, Romania.
2.	Trancoso, I. (2022), Speech as Personally Identifiable Information. Keynote talk at 10th Iberian Conference on Pattern Recognition and Image Analysis (IbPRIA 2022), Aveiro, Portugal. 
3.	Trancoso, I. (2022), Disease Biomarkers in Speech. Keynote talk at 6th IberSpeech, Granada, Spain (November 2022).

---

## Team Members

* Isabel Trancoso (P.I., INESC-ID)
* Bhiksha Raj (P.I., CMU)
* Alberto Abad (Co-P.I., INESC-ID)
* Francisco Teixeira (Ph.D. student)
* Daniel Oliveira (student, February - August 2021)

<img id="Project Timeline" src="https://fsepteixeira.github.io/PrivaDia/assets/team.png" width="75%"/>

## Project Timeline (January-December 2021)

<img id="Project Timeline" src="https://fsepteixeira.github.io/PrivaDia/assets/privadia_timeline.png" width="75%" height="75%"/>

The project has been granted an extension of 6 months, until June 2022.

## Contacts
For further information about our project, please contact us at privadia@hlt.inesc-id.pt.

## Participating and Funding Institutions
<div>
<img id="INESC-ID" src="https://fsepteixeira.github.io/PrivaDia/assets/logos/inesc-id_logo.png" height="125px"/>
<img id="CMU" src="https://fsepteixeira.github.io/PrivaDia/assets/logos/cmu_logo.png" height="125px"/>
<img id="CMU Portugal" src="https://fsepteixeira.github.io/PrivaDia/assets/logos/cmu_portugal_logo.png" height="125px"/>
</div>

