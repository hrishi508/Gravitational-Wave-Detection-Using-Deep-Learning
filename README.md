# What are Gravitational Waves?
Gravitational waves are 'ripples' in space-time caused by some of the most violent and energetic processes in the Universe. These cosmic ripples would travel at the speed of light, carrying with them information about their origins, as well as clues to the nature of gravity itself. Albert Einstein predicted the existence of gravitational waves in 1916 in his general theory of relativity.

The strongest gravitational waves are produced by cataclysmic events such as **colliding black holes**, supernovae, and **colliding neutron stars**. Other waves are predicted to be caused by the rotation of neutron stars that are not perfect spheres, and possibly even the remnants of gravitational radiation created by the Big Bang.

The animation below illustrates how gravitational waves are emitted by two neutron stars as they orbit each other and then coalesce (credit: NASA/Goddard Space Flight Center). Note that gravitational waves themselves are invisible. They are made visible here to illustrate their propagation away from the source.



According to Krastev [1], the groundbreaking discoveries of **gravitational waves** from **binary black-hole mergers** and **coalescing neutron stars** have started a new era of Multi-Messenger Astrophysics. In this project we use various deep-learning techniques to rapidly identify transient gravitational-wave signals from binary neutron star and black-hole mergers in a noisy time series representative of typical gravitational-wave detector data. These results demonstrate the potential of artificial neural networks for real-time detection of gravitational-wave signals from binary neutron star mergers, which is critical for a prompt follow-up and detailed observation of the electromagnetic and astro-particle counterparts accompanying these important transients.

These discoveries were
made possible by the Advanced Laser Interferometer Grav-
itational Wave Observatory (LIGO) and Virgo collabora-
tions. As gravitational-wave detectors increase their sen-
sitivity many more observations, including BBH, binary
neutron star (BNS) and black hole - neutron star (BHNS)
signals are likely to be detected more frequently.

The computational cost of these low-latency GW
searches based on implementations of matched-filtering is
presently such that their extension to the full 9D signal
manifold is computationally prohibitive

Most impor-
tantly, these surveys may miss important GW transients
where a rapid follow-up is critical for successful observation
of their electromagnetic counterparts

due to their fast decay
rate they need to be identified and localized within several
hours after the compact binary merger and promptly ob-
served in the entire electromagnetic spectrum. Therefore,
based on the above considerations, the need arises for new
methods to overcome the limitations and computational
challenges of existing GW detection algorithms, in partic-
ular, approaches to detect in real-time GW signals from
binary neutron star (and black hole-neutron star) mergers
in the full parameter space available to current and future
GW detectors

Deep-learning methods are able to perform
analysis rapidly since the computationally intensive part
of the algorithm is done during the training stage before
the actual data analysis [19], which could make them or-
ders of magnitude faster than conventional match-filtering
techniques

# Versions
1) Python     - 3.6.9
2) GWpy       - 2.1.3
3) PyCBC      - 1.18.3
2) Tensorflow - 2.3.0
3) Keras      - 2.3.1 

# Data Description
describe the data here, give overview about time series data then specifically about gravitational wave data and the types of glitches or noise.
    
# Architecture
Insert best architectures here.

# Results
Insert results here.

# References
1. <p>Chauhan, Y., 2020. Deep Learning Techniques to Make Gravitational Wave Detections from Weak Time-series Data. arXiv preprint arXiv:2007.05889.</p>
2. <p>Krastev, Plamen. (2019). Real-Time Detection of Gravitational Waves from Binary Neutron Stars using Artificial Neural Networks. </p>
3. Razzano, M. and Cuoco, E., 2018. Image-based deep learning for classification of noise transients in gravitational wave detectors. Classical and Quantum Gravity, 35(9), p.095016.
4. Dodia, H., Tandel, H. and D'Mello, L., 2021. SpecGrav--Detection of Gravitational Waves using Deep Learning. arXiv preprint arXiv:2107.03607.
5. Ormiston, R., Nguyen, T., Coughlin, M., Adhikari, R.X. and Katsavounidis, E., 2020. Noise reduction in gravitational-wave data via deep learning. Physical Review Research, 2(3), p.033066.