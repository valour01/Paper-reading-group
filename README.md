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


### 2018-01-09
#### Title: Automated Bug Removal for Software-Defined Networks
##### Authors: Yang Wu, Ang Chen, Andreas Haeberlen, Wenchao Zhou, Boon Thau Loo
Abstract: When debugging an SDN application, diagnosing the problem is merely the first step: the operator must still find a fix that solves the problem, without causing new problems elsewhere. However, most existing debuggers focus exclusively on diagnosis and offer the network operator little or no help with finding an effective fix. Finding a suitable fix is difficult because the number of candidates can be enormous.
In this paper, we propose a step towards automated repair for SDN applications. Our approach consists of two elements. The first is a data structure that we call meta provenance, which can be used to efficiently find good candidate repairs. Meta provenance is inspired by the provenance concept from the database community; however, whereas standard provenance can only reason about changes to data, meta provenance can also reason about changes to programs. The second element is a system that can efficiently backtest a set of candidate repairs using historical data from the network. This is used to eliminate candidate repairs that do not work well, or that cause other problems.
We have implemented a system that maintains meta provenance for SDNs, as well as a prototype debugger that uses the meta provenance to automatically suggest repairs. Results from several case studies show that, for problems of moderate complexity, our debugger can find high-quality repairs within one minute.

[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_09_NSDI_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_09_NSDI_2018/slides.pdf)


### 2018-01-15
#### Title: Supporting Transparent Snapshot for Bare-metal Malware Analysis on Mobile Devices
##### Authors: Le Guan, Shijie Jia, Bo Chen, Fengwei Zhang, Bo Luo, Jingqiang Lin, Peng Liu, Xinyu Xing, Lunxing xia
Abstract: The increasing growth of cybercrimes targeting mobile devices urges an efficient malware analysis platform. With the emergence of evasive malware, which is capable of detecting that it is being analyzed in virtualized environments, bare-metal analysis has become the definitive resort. Existing works mainly focus on extracting the malicious behaviors exposed during bare-metal analysis. However, after malware analysis, it is equally important to quickly restore the system to a clean state to examine the next sample. Unfortunately, state-of-the-art solutions on mobile platforms can only restore the disk, and require a time-consuming system reboot. In addition, all of the existing works require some in-guest components to assist the restoration. Therefore, a kernel-level malware is still able to detect the presence of the in-guest components. We propose Bolt, a transparent restoration mechanism for baremetal analysis on mobile platform without rebooting. Bolt achieves a reboot-less restoration by simultaneously making a snapshot for both the physical memory and the disk. Memory snapshot is enabled by an isolated operating system (BoltOS) in the ARM TrustZone secure world, and disk snapshot is accomplished by a piece of customized firmware (BoltFTL) for flash-based block devices. Because both the BoltOS and the BoltFTL are isolated from the guest system, even kernel-level malware cannot interfere with the restoration. More importantly, Bolt does not require any modifications into the guest system. As such, Bolt is the first that simultaneously achieves efficiency, isolation, and stealthiness to recover from infection due to malware execution. We have implemented a Bolt prototype working with the Android OS. Experimental results show that Bolt can restore the guest system to a clean state in only 2.80 seconds.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_15_ACSAC_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_15_ACSAC_2018/slides.pdf)

### 2018-01-22
#### Title:DIDACache: A Deep Integration of Device and Application for Flash Based Key-Value Caching
##### Authors: Zhaoyan Shen, Feng Chen, Yichen Jia, Zili Shao
Abstract:In recent years, flash-based key-value cache systems have raised high interest in industry, such as Facebook’s McDipper and Twitter’s Fatcache. These cache systems typically use commercial SSDs to store and manage key-value cache data in flash. Such a practice, though simple, is inefficient due to the huge semantic gap between the key-value cache manager and the underlying flash devices. In this paper, we advocate to reconsider the cache system design and directly open device-level details of the underlying flash storage for key-value caching. This co-design approach bridges the semantic gap and well connects the two layers together, which allows us to leverage both the domain knowledge of key-value caches and the unique device properties. In this way, we can maximize the efficiency of key-value caching on flash devices while minimizing its weakness. We implemented a prototype, called DIDACache, based on the Open-Channel SSD platform. Our experiments on real hardware show that we can significantly increase the throughput by 35.5%, reduce the latency by 23.6%, and remove unnecessary erase operations by 28%. 


[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_22_FAST_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_January/01_22_FAST_2018/slides.pdf)


### 2018-02-02
#### Title: Generating Tests by Example
##### Authors: Hila Peleg, Dan Rasin, Eran Yahav
Abstract:Property-based testing is a technique combining parametric tests with value generators, to create an efficient and maintainable way to test general specifications. To test the program, property-based testing randomly generates a large number of inputs defined by the generator to check whether the test-assertions hold.
We present a novel framework that synthesizes property-based tests from existing unit tests. Projects often have a suite of unit tests that have been collected over time, some of them checking specific and subtle cases. Our approach leverages existing unit tests to learn property-based tests that can be used to increase value coverage by orders of magnitude. Further, we show that our approach: (i) preserves the subtleties of the original test suite; and (ii) produces properties that cover a greater range of inputs than those in the example set.
The main idea is to use abstractions to over-approximate the concrete values of tests with similar structure. These abstractions are then used to produce appropriate value generators that can drive the synthesized property-based test.
We present JARVIS, a tool that synthesizes property-based tests from unit tests, while preserving the subtleties of the original unit tests. We evaluate JARVIS on tests from Apache projects, and show that it preserves these interesting tests while increasing value coverage by orders of magnitude.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/02_02_VMCAI_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/02_02_VMCAI_2018/slides.pdf)


### 2018-02-06
#### Title: Precise and Scalable Detection of Double-Fetch Bugs in OS Kernels
##### Authors: Meng Xu, Chenxiong Qian, Kangjie Lu, Michael Backes, Taesoo Kim
Abstract: During system call execution, it is common for operating system kernels to read userspace memory multiple times (multi-reads). A critical bug may exist if the fetched userspace memory is subject to change across these reads, i.e., a race condition, which is known as a double-fetch bug. Prior works have attempted to detect these bugs both statically and dynamically. However, due to their improper assumptions and imprecise definitions regarding double-fetch bugs, their multi-read detection is inherently limited and suffers from significant false positives and false negatives. For example, their approach is unable to support device emulation, inter-procedural analysis, loop handling, etc. More importantly, they completely leave the task of finding real double-fetch bugs from the haystack of multi-reads to manual verification, which is expensive if possible at all. In this paper, we first present a formal and precise definition of double-fetch bugs and then implement a static analysis system - Deadline - to automatically detect double-fetch bugs in OS kernels. Deadline uses static program analysis techniques to systematically find multi-reads through out the kernel and employs specialized symbolic checking to vet each multi-read for double-fetch bugs. We apply Deadline to Linux and FreeBSD kernels and find 23 new bugs in Linux and one new bug in FreeBSD. We further propose four generic strategies to patch and prevent double-fetch bugs based on our study and the discussion with kernel maintainers.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/02_06_SP_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/02_06_SP_2018/slides.pdf)


### 2018-03-18
#### Title: Decentralized Action Integrity for Trigger-Action IoT Platforms
##### Authors: Earlence Fernandes, Amir Rahmati, Jaeyeon Jung, Atul Prakash
Abstract: Trigger-Action platforms are web-based systems that enable users to create automation rules by stitching together online services representing digital and physical resources using OAuth tokens. Unfortunately, these platforms introduce a longrange large-scale security risk: If they are compromised, an attacker can misuse the OAuth tokens belonging to a large number of users to arbitrarily manipulate their devices and data. We introduce Decentralized Action Integrity, a security principle that prevents an untrusted trigger-action platform from misusing compromised OAuth tokens in ways that are inconsistent with any given user’s set of trigger-action rules. We present the design and evaluation of Decentralized Trigger-Action Platform (DTAP), a trigger-action platform that implements this principle by overcoming practical challenges. DTAP splits currently monolithic platform designs into an untrusted cloud service, and a set of user clients (each user only trusts their client). Our design introduces the concept of Transfer Tokens (XTokens) to practically use finegrained rule-specific tokens without increasing the number of OAuth permission prompts compared to current platforms. Our evaluation indicates that DTAP poses negligible overhead: it adds less than 15ms of latency to rule execution time, and reduces throughput by 2.5%.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/03_18_NDSS_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/03_18_NDSS_2018/slides.pdf)



### 2018-03-20
#### Title: K-Miner: Uncovering Memory Corruption in Linux
##### Authors: David Gens,Simon Schmitt, Lucas Davi,† Ahmad-Reza Sadeghi
Abstract: Operating system kernels are appealing attack targets: compromising the kernel usually allows attackers to bypass all deployed security mechanisms and take control over the entire system. Commodity kernels, like Linux, are written in low-level programming languages that offer only limited type and memory-safety guarantees, enabling adversaries to launch sophisticated run-time attacks against the kernel by exploiting memory-corruption vulnerabilities. Many defenses have been proposed to protect operating systems at run time, such as control-flow integrity (CFI). However, the goal of these run-time monitors is to prevent exploitation as a symptom of memory corruption, rather than eliminating the underlying root cause, i.e., bugs in the kernel code. While finding bugs can be automated, e.g., using static analysis, all existing approaches are limited to local, intra-procedural checks, and face severe scalability challenges due to the large kernel code base. Consequently, there currently exist no tools for conducting global static analysis of operating system kernels. In this paper, we present K-Miner, a new framework to efficiently analyze large, commodity operating system kernels like Linux. Our novel approach exploits the highly standardized interface structure of the kernel code to enable scalable pointer analysis and conduct global, context-sensitive analysis. Through our inter-procedural analysis we show that K-Miner systematically and reliably uncovers several different classes of memory-corruption vulnerabilities, such as dangling pointers, user-after-free, double-free, and double-lock vulnerabilities. We thoroughly evaluate our extensible analysis framework, which leverages the popular and widely used LLVM compiler suite, for the current Linux kernel and demonstrate its effectiveness by reporting several memory-corruption vulnerabilities.


[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/03_20_NDSS_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/03_20_NDSS_2018/slides.pdf)



### 2018-03-27
#### Title: Superset Disassembly: Statically Rewriting x86 Binaries Without Heuristics
##### Authors: Erick Bauman, Zhiqiang Lin, Kevin W. Hamlen
Abstract: Static binary rewriting is a core technology for many systems and security applications, including profiling, optimization, and software fault isolation. While many static binary rewriters have been developed over the past few decades, most make various assumptions about the binary, such as requiring correct disassembly, cooperation from compilers, or access to debugging symbols or relocation entries. This paper presents MULTIVERSE, a new binary rewriter that is able to rewrite Intel CISC binaries without these assumptions. Two fundamental techniques are developed to achieve this: (1) a superset disassembly that completely disassembles the binary code into a superset of instructions in which all legal instructions fall, and (2) an instruction rewriter that is able to relocate all instructions to any other location by mediating all indirect control flow transfers and redirecting them to the correct new addresses. A prototype implementation of MULTIVERSE and evaluation on SPECint 2006 benchmarks shows that MULTIVERSE is able to rewrite all of the testing binaries with a reasonable runtime overhead for the new rewritten binaries. Simple static instrumentation using MULTIVERSE and its comparison with dynamic instrumentation shows that the approach achieves better average performance. Finally, the security applications of MULTIVERSE are exhibited by using it to implement a shadow stack


.
[article](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/03_28_NDSS_2018/paper.pdf)
[slides](https://github.com/valour01/Paper-reading-group/blob/master/2018_February/03_28_NDSS_2018/slides.pdf)




