#Paper-reading-group


### 2017-12-10
#### Title: Dynamic Hooks: Hiding Control Flow Changes within Non-Control Data
##### Authors: Sebastian Vogl, Robert Gawlik, Behrad Garmany, Thomas Kittel, Jonas Pfoh, Claudia Eckert, Thorsten Holz
Abstract:Generally speaking, malicious code leverages hooks within a system to divert the control flow. Without them, an attacker is blind to the events occurring in the system, rendering her unable to perform malicious activities (e.g., hiding of files or capturing of keystrokes). However, while hooks are an integral part of modern attacks, they are at the same time one of their biggest weaknesses: Even the most sophisticated attack can be easily identified if one of its hooks is found. In spite of this fact, hooking mechanisms have remained almost unchanged over the last years and still rely on the persistent modification of code or control data to divert the control flow. As a consequence, hooks represent an abnormality within the system that is permanently evident and can in many cases easily be detected as the hook detection mechanisms of recent years amply demonstrated.

In this paper, we propose a novel hooking concept that we refer to as dynamic hooking. Instead of modifying persistent control data permanently, this hooking mechanisms targets transient control data such as return addresses at run-time. The hook itself will thereby reside within non-control data and remains hidden until it is triggered. As a result, there is no evident connection between the hook and the actual control flow change, which enables dynamic hooks to successfully evade existing detection mechanisms. To realize this idea, dynamic hooks make use of exploitation techniques to trigger vulnerabilities at run-time. Due to this approach, dynamic hooks cannot only be used to arbitrarily modify the control flow, but can also be applied to conduct non-control data attacks, which makes them more powerful than their predecessors. We implemented a prototype that makes uses of static program slicing and symbolic execution to automatically extract paths for dynamic hooks that can then be used by a human expert for their realization. To demonstrate this, we used the output provided by our prototype to implement concrete examples of dynamic hooks for both modern Linux and Windows kernels.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_10_Security_2014/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_10_Security_2014/slides.pdf)


### 2017-12-16
#### Title: pbSE: Phase-Based Symbolic Execution

[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_16_DSN_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_16_DSN_2017/slides.pdf)


### 2017-12-20
#### Title: The Efficient Server Audit Problem, Deduplicated Re-execution, and the Web

[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_20_SOSP_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_20_SOSP_2017/slides.pdf)


### 2017-12-29
#### Title: Software Vulnerability Analysis and Discovery Using Machine-Learning and Data-Mining Techniques: A Survey

[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_29_CSUR_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_29_CSUR_2017/slides.pdf)
