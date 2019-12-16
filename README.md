# Ensemble Adversarial Black-Box Attacks against Deep Learning Systems
## Main work and contributions
Deep learning models, e.g., state-of-the-art convolutional neural networks (CNNs), have been widely applied into security-sensitivity tasks, such as facial recognition, automated driving, etc. Then their vulnerability analysis is an emergent topic, especially for black-box attacks, where adversaries do not know the model internal architectures or training parameters.

This paper fully investigates the black-box attack strategies, which always train a substitute model to craft adversarial examples, and these adversarial examples can be transfered to disorder target models due to the transferability. However, conventional single-substitute attack strategies are easily defended by existed defense mechanism, e.g., ensemble adversarial training technology, and achieve unsatisfactory attack performance in black-box attack scenario.

In this paper, the authors attempt to ensemble multiple pre-trained substitute models to produce adversarial examples with more powerful transferability in the form of selective cascade ensemble and stack parallel ensemble. Moreover, potential factors that contribute to the high-efficiency attacks are presented from three perspectives: the transferability of substitutes, the diversity of substitutes and the number of substitutes. Two classical measurements, Success rate and Transfer rate are used to analyze the vulnerability of deep learning models in black-box attack scenario. Two common pairwise and non-pairwise diversity measures are adopted to explore the relationship between the diversity in substitutes ensembles and transferability of crafted adversarial examples. Experimental results demonstrate that proposed ensemble adversarial attack strategies can successfully attack the deep learning models trained with ensemble adversarial training defense mechanism. This paper also indicates the diversity and the number of substitutes k for ensembles are important factors to affect the transferability of generated adversarial examples..

In our paper, due to limited space , some experimental results are not presented, we show the entire experimental results as follows:

(1) The transferability of adversarial examples generated by each substitute model and cascading or paralleling any k substitutes (e.g. k=3,5) are illustrated in Fig.1.

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image013.png" width = "280px" height="200px" alt="(a)USPS" > 
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image001.png" width = "280px"  height="200px" alt="(b)MNIST" > 
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image008.png" width = "280px"  height="200px" alt="(c)GTSRB" >
</div>

Fig.1. Transfer rate of adversarial examples crafted by SCES and SPES under different perturbation magnitude α on (left)USPS, (center)MNIST and (right)GTSRB.

(2) Fig. 2, 3, 4. demonstrates that our proposed ensemble-based black-box attack strategies are still aggressive to target classifier trained with adversarial training and ensemble adversarial training defense mechanism.

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image016.png" width = "300" height="200px" alt="(a)Black-box model trained with adversarial training" > <img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image017.png" width = "300"  height="200px" alt="(b)Black-box model trained with ensemble adversarial training" >
</div>

Fig.2. Defense performance of black-box model trained with (left)adversarial training and (right)ensemble adversarial training against different attacks on USPS.

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image002.png" width = "300" height="200px" alt="(a)Black-box model trained with adversarial training" > <img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image005.png" width = "300"  height="200px" alt="(b)Black-box model trained with ensemble adversarial training" >
</div>

Fig.3. Defense performance of black-box model trained with (left)adversarial training and (right)ensemble adversarial training against different attacks on MNIST.  

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image009.png" width = "300" height="200px" alt="(a)Black-box model trained with adversarial training" > <img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image012.png" width = "300"  height="200px" alt="(b)Black-box model trained with ensemble adversarial training" >
</div>

Fig.4. Defense performance of black-box model trained with (left)adversarial training and (right)ensemble adversarial training against different attacks on GTSRB.

Transfer rate of adversarial examples crafted by SCES and SPES with k=1, 3 and 5 under different perturbation magnitude α in FGSM are shown in Fig.5., Fig.6. and Fig.7.  

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image003.png" width = "300" height="200px" alt="(a)SCES" > <img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image014.png" width = "300"  height="200px" alt="(b)SPES" >
</div>

Fig.5. Transfer rate of adversarial examples crafted by (left)SCES and (right)SPES with k=1, 3 and 5 under different perturbation magnitude α on USPS.

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image015.png" width = "300" height="200px" alt="(a)SCES" > <img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image004.png" width = "300"  height="200px" alt="(b)SPES" >
</div>

Fig.6. Transfer rate of adversarial examples crafted by (left)SCES and (right)SPES with k=1, 3 and 5 under different perturbation magnitude α on MNIST.

<div align="center">
<img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image010.png" width = "300" height="200px" alt="(a)SCES" > <img src="https://github.com/HangJie720/Ensemble_Adversarial_Attack/blob/master/img/image011.png" width = "300"  height="200px" alt="(b)SPES" >
</div>

Fig. 7. Transfer rate of adversarial examples crafted by (left)SCES and (right)SPES with k=1, 3 and 5 under different perturbation magnitude α on GTSRB. 
                                                     
## Part work
Our part work has been appeared in "Delving into Diversity in Substitute Ensembles and Transferability of Adversarial Examples", which can be downloaded by: https://link.springer.com/chapter/10.1007/978-3-030-04182-3_16

## Acknowledgement
Participants:: LI-DATA Lab; Professor Yun Li, Ph.D, KeJi Han, Ph.D Candidate; Hui Chen, Master;

Referencing to the following projects:
- [cleverhans](https://github.com/tensorflow/cleverhans)

- [tensorflow](https://github.com/tensorflow/tensorflow)

- [ensemble adversarial training](https://github.com/ftramer/ensemble-adv-training)

- [Carlini & Wagner Attack](https://github.com/carlini/nn_robust_attacks)

## Reference
1. Babaee M., Dinh D T., Rigoll G.: A deep convolutional neural network for video sequence background subtraction. Pattern Recognition, 76:635–649, 2018. 2. Schroff, F., Kalenichenko, D., Philbin J.: FaceNet: A unified embedding for face recognition and clustering. In: The 2015 IEEE Conference on Computer Vision and Pattern Recognition(CVPR), pp:815-823. IEEE Press, New York, 2015.

3. Chu W., Li W W.: Manga face detection based on deep neural networks fusing global and local information. Pattern Recognition, 86:62–72, 2019.

4. Wang Q., Fan HJ., Sun G., Cong Y., &Tang YD.: Laplacian pyramid adversarial network for face completion. Pattern Recognition, 88:493-505, 2019.

5. Biggio B., Roli F.: Wild Patterns: Ten years after the rise of adversarial machine learning. Pattern Recognition, 84:317–331, 2018.

6. Evtimov, I., Eykholt, K., Fernandes, E.: Robust physical-world attacks on deep learning visual classification. In: The 2018 IEEE Conference on Computer Vision and Pattern Recognition(CVPR), pp:1625-1634. IEEE Press, New York, 2018.

7. Sharif, M., Bhagavatula, S., Bauer, L., Michael, K.R.: Accessorize to a crime: Real and stealthy attacks on state-of-the-art face recognition. In: 2016 ACM SIGSAC Conference on Computer and Communications Security(CCS), pp: 1528-1540. ACM, New York, 2016.

8. Grosse, K., Papernot, N., Manoharan, P., Backes, Michael., McDaniel, P.: Adversarial examples for malware detection. In: The 2017 European Symposium on Research in Computer Security(ESORICS), pp: 62-79. Springer, Heidelberg , 2017.

9. Szegedy, C., Zaremba, W., Sutskever, I., Bruna, J., Erhan, D., Goodfellow, I., Fergus, R.: Intriguing properties of neural networks. In: The 2nd International Conference on Learning Representations (ICLR), 2014.

10. Papernot, N., McDaniel, P.: Transferability in machine learning: from phenomena to blackbox attacks using adversarial samples. arXiv:1605.07277, 2016.

11. Liu, Y., Chen, X., Liu, C., Song, D.: Delving into transferable adversarial examples and black-box attacks. In: 5th International Conference on Learning Representations (ICLR), 2017. 32

12. Papernot N., Mcdaniel P., Goodfellow I.: Practical Black-Box Attacks against Machine Learning[J]. Proceedings of the 2017 ACM on Asia Conference on Computer and Communications Security, (ASIA CCS), pp. 506-519, 2017.

13. Papernot, N., Mcdaniel, P., Sinha, A., Wellman, M.: Towards the science of security and privacy in machine learning. arXiv preprint arXiv:1611.03814, 2016.

14. Meng, D.Y., Chen, H.: MagNet: a Two-pronged Defense against Adversarial Examples. In: ACM SIGSAC Conference on Computer and Communications Security(CCS), pp: 135-147. ACM, New York, 2017.

15. Wang, Q.L., Guo, W.B., Zhang, K.X., Ororbia Ii, A. G., Xing, X., Liu, X.: Adversary resistant deep neural networks with an application to malware detection. In: The 23rd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining(KDD), pp: 1145-1153. ACM, New York, 2017.

16. Bhagoji, A, J., Cullina, D., Mittal, P.: Dimensionality reduction as a defense against evasion attacks on machine learning classifiers. arXiv preprint arXiv:1704.02654, 2017.

17. Tramèr, F., Kurakin, A., Papernot, N., Boneh, D., McDaniel, P.: Ensemble adversarial training: Attacks and defenses. In: The 6th International Conference on Learning Representations (ICLR), 2018.

18. Goodfellow, I., Shlens, J., Szegedy, C.: Explaining and harnessing adversarial examples. In: The 3rd International Conference on Learning Representations (ICLR), 2015.

19. Kurakin, A., Goodfellow, I., Bengio, S.: Adversarial machine learning at scale. In: The 5th International Conference on Learning Representations (ICLR), 2017.

20. Hang, J., Han, K.J., Li, Y.: Delving into diversity in substitute ensembles and transferability of adversarial examples. In: The 25th International Conference on Neural Information Processing(ICONIP), pp: 175-187. Spring, Heidelberg, 2018. 21. Madry, A., Makelov, A., Schmidt, L., Tsipras, D., Vladu, A.: Towards deep learning models resistant to adversarial attacks. In: The 6th International Conference on Learning Representations (ICLR), 2018.

22. Kurakin, K., Goodfellow, J., Bengio, S.: Adversarial examples in the physical world. In: The 5th International Conference on Learning Representations (ICLR), 2017.

23. Shaham U., Yamada Y., Negahban S.: Understanding adversarial training: Increasing local stability of neural nets through robust optimization. Neurocomputing, vol. 307: 195-204, 2018

24. Athalye, A., Carlini, N., Wagner, D.: Obfuscated gradients give a false sense of security: Circumventing defenses to adversarial examples. In: The 6th International Conference on Learning Representations (ICLR), 2018.tutorial

25. Sinha, A., Namkoong, H., Duchi, J.: Certifying some distributional robustness with principled adversarial training. In: The 6th International Conference on Learning Representations (ICLR), 2018.

26. Tramèr F., Papernot, N., Goodfellow, I., Boneh, D., McDaniel, P.: The space of transferable adversarial examples. arXiv:1704.03453, 2017.

27. Abadi, M., Barham, P., Chen, J. M., et al.: TensorFlow: A System for Large-Scale Machine Learning. In: The USENIX Symposium on Operating Systems Design and Implementation (OSDI 16), pp: 265-283, 2016.

28. Abadi, M., Agarwal, A., Barham, P., et al.: TensorFlow: Large-scale machine learning on distributed heterogeneous systems. Software available from https://www.tensorflow.org, 2015.

29. Papernot, N., Faghri, F., Carlini, N., Goodfellow, I., Feinman, R., Kurakin A., et al.: CleverHans v2.1.0: an adversarial machine learning library.

30. Kuncheva L I., Whitaker C J.: Measures of diversity in classifier ensembles and their relationship with the ensemble accuracy. Machine Learning, 51(2):181-207, 2003.


