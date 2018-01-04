# Paper-reading-group

### 2017-11-03
#### Title: TaintScope: A Checksum-Aware Directed Fuzzing Tool for Automatic Software Vulnerability Detection
##### Authors: Tielei Wang, Tao Wei, Guofei Gu, Wei Zou
Abstract:Fuzz testing has proven successful in finding security vulnerabilities in large programs. However, traditional fuzz testing tools have a well-known common drawback: they are ineffective if most generated malformed inputs are rejected in the early stage of program running, especially when target programs employ checksum mechanisms to verify the integrity of inputs. In this paper, we present TaintScope, an automatic fuzzing system using dynamic taint analysis and symbolic execution techniques, to tackle the above problem. TaintScope has several novel contributions: 1) TaintScope is the first checksum-aware fuzzing tool to the best of our knowledge. It can identify checksum fields in input instances, accurately locate checksum-based integrity checks by using branch profiling techniques, and bypass such checks via control flow alteration. 2) TaintScope is a directed fuzzing tool working at X86 binary level (on both Linux and Window). Based on fine-grained dynamic taint tracing, TaintScope identifies which bytes in a well-formed input are used in security-sensitive operations (e.g., invoking system/library calls) and then focuses on modifying such bytes. Thus, generated inputs are more likely to trigger potential vulnerabilities. 3) TaintScope is fully automatic, from detecting checksum, directed fuzzing, to repairing crashed samples. It can fix checksum values in generated inputs using combined concrete and symbolic execution techniques. We evaluate TaintScope on a number of large real-world applications. Experimental results show that TaintScope can accurately locate the checksum checks in programs and dramatically improve the effectiveness of fuzz testing. TaintScope has already found 27 previously unknown vulnerabilities in several widely used applications, including Adobe Acrobat, Google Picasa, Microsoft Paint, and ImageMagick. Most of these severe vulnerabilities have been confirmed by Secunia and oCERT, and assigned CVE identifiers (such as CVE-2009-1882, CVE-2009-2688). Corresponding patches from vendors are released or in progress based on our reports.



[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_03_SP_2010/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_03_SP_2010/slides.pdf)


### 2017-11-09
#### Title: DART: directed automated random testing
##### Authors: Patrice Godefroid, Nils Klarlund, Koushik Sen
Abstract:We present a new tool, named DART, for automatically testing software that combines three main techniques: (1) automated extraction of the interface of a program with its external environment using static source-code parsing; (2) automatic generation of a test driver for this interface that performs random testing to simulate the most general environment the program can operate in; and (3) dynamic analysis of how the program behaves under random testing and automatic generation of new test inputs to direct systematically the execution along alternative program paths. Together, these three techniques constitute Directed Automated Random Testing, or DART for short. The main strength of DART is thus that testing can be performed completely automatically on any program that compiles -- there is no need to write any test driver or harness code. During testing, DART detects standard errors such as program crashes, assertion violations, and non-termination. Preliminary experiments to unit test several examples of C programs are very encouraging.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_09_PLDI_2005/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_09_PLDI_2005/slides.pdf)


### 2017-11-18
#### Title: Semi-automated discovery of server-based information oversharing vulnerabilities in Android applications
##### Authors: William Koch, Abdelberi Chaabane, Manuel Egele, William Robertson, Engin Kirda
Abstract:Modern applications are often split into separate client and server tiers that communicate via message passing over the network. One well-understood threat to privacy for such applications is the leakage of sensitive user information either in transit or at the server. In response, an array of defensive techniques have been developed to identify or block unintended or malicious information leakage. However, prior work has primarily considered privacy leaks originating at the client directed at the server, while leakage in the reverse direction -- from the server to the client -- is comparatively under-studied. The question of whether and to what degree this leakage constitutes a threat remains an open question. We answer this question in the affirmative with Hush, a technique for semi-automatically identifying Server-based InFormation OvershariNg (SIFON) vulnerabilities in multi-tier applications. In particular, the technique detects SIFON vulnerabilities using a heuristic that overshared sensitive information from server-side APIs will not be displayed by the application's user interface. The technique first performs a scalable static program analysis to screen applications for potential vulnerabilities, and then attempts to confirm these candidates as true vulnerabilities with a partially-automated dynamic analysis. Our evaluation over a large corpus of Android applications demonstrates the effectiveness of the technique by discovering several previously-unknown SIFON vulnerabilities in eight applications.

[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_18_ISSTA_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_18_ISSTA_2017/slides.pdf)



### 2017-11-25
#### Title : Symbolic Complexity Analysis Using Context-Preserving Histories
##### Authors: Kasper Luckow, Rody Kersten, Corina Pasareanu
Abstract:We propose a technique based on symbolic execution for analyzing the algorithmic complexity of programs. The technique uses an efficient guided analysis to compute bounds on the worst-case complexity (for increasing input sizes) and to generate test values that trigger the worst-case behaviors. The resulting bounds are fitted to a function to obtain a prediction of the worst-case program behavior at any input sizes. Comparing these predictions to the programmers' expectations or to theoretical asymptotic bounds can reveal vulnerabilities or confirm that a program behaves as expected. To achieve scalability we use path policies to guide the symbolic execution towards worst-case paths. The policies are learned from the worst-case results obtained with exhaustive exploration at small input sizes and are applied to guide exploration at larger input sizes, where un-guided exhaustive exploration is no longer possible. To achieve precision we use path policies that take into account the history of choices made along the path when deciding which branch to execute next in the program. Furthermore, the history computation is context-preserving, meaning that the decision for each branch depends on the history computed with respect to the enclosing method. We implemented the technique in the Symbolic PathFinder tool. We show experimentally that it can find vulnerabilities in complex Java programs and can outperform established symbolic techniques.

[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_25_ICST_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_November/11_25_ICST_2017/slides.pdf)



### 2017-12-01
#### Title : Secure Information Flow Verification with Mutable Dependent Types
##### Authors: Andrew Ferraiuolo, Weizhe Hua, Andrew C.Myers, G.Edward Suh
Abstract:This paper presents a novel secure hardware description language (HDL) that uses an information flow type system to ensure that hardware is secure at design time. The novelty of this HDL lies in its ability to securely share hardware modules and storage elements across multiple security levels. Unlike previous secure HDLs, the new HDL enables secure sharing at a fine granularity and without implicitly adding hardware for security enforcement; this is important because the implicitly added hardware can break functionality and harm efficiency. The new HDL enables practical hardware designs that are secure, correct, and efficient. We demonstrate the practicality of the new HDL by using it to design and type-check a synthesizable pipelined processor implementation that support protection rings and instructions that change modes.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_01_DAC_2017/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2017_December/12_01_DAC_2017/slides.pdf)


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

### 2018-01-03
#### Title: Automated Attack Discovery in TCP Congestion Control Using a Model-guided Approach
##### Authors: Samuel Jero, Endadul Hoque, David Choffnes, Alan Mislove, Cristina Nita-Rotaru
Abstract: One of the most important goals of TCP is to ensure fairness and prevent congestion collapse by implementing congestion control. Various attacks against TCP congestion control have been reported over the years, most of which have been discovered through manual analysis. In this paper, we propose an automated method that combines the generality of implementation-agnostic fuzzing with the precision of runtime analysis to find attacks against implementations of TCP congestion control. It uses a model-guided approach to generate abstract attack strategies, by leveraging a state machine model of TCP congestion control to find vulnerable state machine paths that an attacker could exploit to increase or decrease the throughput of a connection to his advantage. These abstract strategies are then mapped to concrete attack strategies, which consist of sequences of actions such as injection or modification of acknowledgements and a logical time for injection. We design and implement a virtualized platform, TCPWN, that consists of a a proxy-based attack injector and a TCP congestion control state tracker that uses only network traffic to create and inject these concrete attack strategies. We evaluated 5 TCP implementations from 4 Linux distributions and Windows 8.1. Overall, we found 11 classes of attacks, of which 8 are new.

[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_03_NDSS_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_Januaru/01_03_NDSS_2018/slides.pdf)
