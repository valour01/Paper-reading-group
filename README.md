# Paper-reading-group


### 2017-12-10
#### Title: Dynamic Hooks: Hiding Control Flow Changes within Non-Control Data
##### Authors: Sebastian Vogl, Robert Gawlik, Behrad Garmany, Thomas Kittel, Jonas Pfoh, Claudia Eckert, Thorsten Holz
Abstract:Generally speaking, malicious code leverages hooks within a system to divert the control flow. Without them, an attacker is blind to the events occurring in the system, rendering her unable to perform malicious activities (e.g., hiding of files or capturing of keystrokes). However, while hooks are an integral part of modern attacks, they are at the same time one of their biggest weaknesses: Even the most sophisticated attack can be easily identified if one of its hooks is found. In spite of this fact, hooking mechanisms have remained almost unchanged over the last years and still rely on the persistent modification of code or control data to divert the control flow. As a consequence, hooks represent an abnormality within the system that is permanently evident and can in many cases easily be detected as the hook detection mechanisms of recent years amply demonstrated.

In this paper, we propose a novel hooking concept that we refer to as dynamic hooking. Instead of modifying persistent control data permanently, this hooking mechanisms targets transient control data such as return addresses at run-time. The hook itself will thereby reside within non-control data and remains hidden until it is triggered. As a result, there is no evident connection between the hook and the actual control flow change, which enables dynamic hooks to successfully evade existing detection mechanisms. To realize this idea, dynamic hooks make use of exploitation techniques to trigger vulnerabilities at run-time. Due to this approach, dynamic hooks cannot only be used to arbitrarily modify the control flow, but can also be applied to conduct non-control data attacks, which makes them more powerful than their predecessors. We implemented a prototype that makes uses of static program slicing and symbolic execution to automatically extract paths for dynamic hooks that can then be used by a human expert for their realization. To demonstrate this, we used the output provided by our prototype to implement concrete examples of dynamic hooks for both modern Linux and Windows kernels.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_10_Security_2014/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_10_Security_2014/slides.pdf)


### 2017-12-16
#### Title: pbSE: Phase-Based Symbolic Execution
##### Authors: Qixue Xiao, Yu Chen, Chengang Wu, Kang Li, Junjie Mao, Shize Guo, Yuanchun Shi
Abstract:The study of software bugs has long been a key area in software security. Dynamic symbolic execution, in exploring the program's execution paths, finds bugs by analyzing all potential dangerous operations. Due to its high coverage and abilities to generate effective testcases, dynamic symbolic execution has attracted wide attention in the research community. However, the success of dynamic symbolic execution is limited due to complex program logic and its difficulty to handle large symbolic data. In our experiments we found that phase-related features of a program often prevents dynamic symbolic execution from exploring deep paths. On the basis of this discovery, we proposed a novel symbolic execution technology guided by program phase characteristics. Compared to KLEE, the most well-known symbolic execution approach, our method is capable of covering more code and discovering more bugs. We designed and implemented pbSE system, which was used to test several commonly used tools and libraries in Linux. Our results showed that pbSE on average covers code twice as much as what KLEE does, and we discovered 21 previously unknown vulnerabilities by using pbSE, out of which 7 are assigned CVE IDs.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_16_DSN_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_16_DSN_2017/slides.pdf)


### 2017-12-20
#### Title: The Efficient Server Audit Problem, Deduplicated Re-execution, and the Web
##### Authors: Cheng Tan, Lingfan Yu, Joshua B. Leners, Michael Walfish
Abstract:You put a program on a concurrent server, but you don't trust the server; later, you get a trace of the actual requests that the server received from its clients and the responses that it delivered. You separately get logs from the server; these are untrusted. How can you use the logs to efficiently verify that the responses were derived from running the program on the requests? This is the Efficient Server Audit Problem, which abstracts real-world scenarios, including running a web application on an untrusted provider. We give a solution based on several new techniques, including simultaneous replay and efficient verification of concurrent executions. We implement the solution for PHP web applications. For several applications, our verifier achieves 5.6-10.9x speedup versus simply re-executing, with <10% overhead for the server.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_20_SOSP_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_20_SOSP_2017/slides.pdf)


### 2017-12-29
#### Title: Software Vulnerability Analysis and Discovery Using Machine-Learning and Data-Mining Techniques: A Survey
##### Authors: Seyed Mohammad Ghaffarian, Hamid Reza Shahriari
Abstract:Software security vulnerabilities are one of the critical issues in the realm of computer security. Due to their potential high severity impacts, many different approaches have been proposed in the past decades to mitigate the damages of software vulnerabilities. Machine-learning and data-mining techniques are also among the many approaches to address this issue. In this article, we provide an extensive review of the many different works in the field of software vulnerability analysis and discovery that utilize machine-learning and data-mining techniques. We review different categories of works in this domain, discuss both advantages and shortcomings, and point out challenges and some uncharted territories in the field.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_29_CSUR_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_29_CSUR_2017/slides.pdf)
