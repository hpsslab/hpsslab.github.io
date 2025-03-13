---
title: "memclash"
layout: textlay
excerpt: "𝕙𝘆𝕡𝗲𝕤𝘆𝕤 Lab at Colorado School of Mines."
sitemap: false
permalink: /memclash.html
---

![]({{ site.url }}{{ site.baseurl }}/images/logopic/memclash.png){: style="width: 200px; float: left; margin: 0px  12px"}
# Mem-Clash: Shared Memory Related Security Challenges in Mobile Computing Platforms

![]({{ site.url }}{{ site.baseurl }}/images/pubpic/memclash3.png){: style="width: 450px; float: right; margin: 0px  12px"}
We unveil a new critical side-channel leakage based on the memory-access contention occurring when multiple applications execute together in a shared memory multi-processor system. Leveraging this vulnerability, an adversary could build attacks that are concealed within third-party applications in mobile app stores and executed without requiring special privileges or compromised hardware.

This project, Mem-Clash, develops a framework to better understand the vulnerabilities, and investigates several protection mechanisms for mobile shared memory systems. Mem-Clash will enable researchers and system developers to achieve full performance  benefits of multi-accelerator SoCs while protecting their intellectual property in mobile and embedded systems.

![]({{ site.url }}{{ site.baseurl }}/images/pubpic/memclash1.png){: style="width: 550px; float: left; margin: 0px  12px"}
An overview of Mem-Clash: Our attack leverages the shared memory access footprint left by the Neural Network (NN) layers  running within and across accelerators. We first characterize this leaked information for various NN layer and accelerator types. 

We then create a novel memory contention-based leakage detection (MCLD) mechanism. MCLD builds victim network's signatures by detecting its memory BW demand. Using these signatures, we employ attacks to extract hyper-parameters and classification information from victim NNs. 

![]({{ site.url }}{{ site.baseurl }}/images/pubpic/memclash2.png){: style="width: 300px; float: right; margin: 0px  12px"}
Memory BW sensitivity: When VGG NN runs on GPU, perceived BW of the sensing app drops, depending on the executing layers’ memory demand. Moreover, transitions between accelerators cause the sensing application’s perceived BW to be reduced further.

Contributions of our project:
(I) We explore new profiling and analysis techniques to exploit the unique contention characteristics of different accelerators sharing the same system memory. 
(II) We utilize the discovered vulnerabilities to build reverse-engineering, information extraction and denial-of-service based attackers which can be deployed on commonly used mobile app stores without requiring any special permissions and/or compromised hardware. 
(III) We investigate various countermeasures consisting of new memory controller scheduling policies and randomization-based approaches that obfuscate MCLD signatures. 
