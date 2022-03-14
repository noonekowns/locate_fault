# Locating Fault without Comparison to Source File
## Project summary
Bugs can lead to wrong process logic, unpredicted behaviors, program crashes, and even economic loss when they occur in real applications. To improve software quality, most software projects introduce issue trackers (e.g., Bugzilla[1]) to manage bug reports. When a bug is found, it can be reported to an issue tracker. After that, programmers can be notified and then fix the reported bug. Given a bug report, a most important task is to locate its faulty files. The process is time-consuming and labor-intensive, especially for those large projects. As the rapid growth of the number and the size of software, it can be even worse. To reduce the labor and the time consumption, IR-based fault localization approaches [2, 3, 4] have been intensively studied in the past decade.

Given a bug report, IR-based fault localization approaches compare the bug report with the source files to locate its faulty files. As source files keep changing with appended commits during software evolution, these approaches should choose a commit to get source file contents for comparison. As source files are constantly under maintenance, programmers typically select files that are quite different from researchers for comparison. As a result, the true effectiveness in practice is significantly different from what were reported in their papers. We call this problem as the robustness problem of IR-based approaches.

The robustness problem is inherent for IR-based approaches. To bypass this problem, we propose a novel research direction that makes fault localization without comparison to source files. Our direction is based on our observation that if a bug report mentions same words as a previous issue report, a same source file tend to be revised to solve issues. To illustrate our new direction, we propose DisBL and evaluate it on benchmarks and in the wild. The results show that DisBL is sufficiently effective as a research tool, especially when it is the first approach in a novel research direction.

## Dataset
Our dataset is stored in the dataset folder.

## Evaluation Results
### Overall Effectiveness
Our recommendations are provided in results/recommendations. In summary, even without the source files of buggy versions, DISBL achieved actuary values that are similar to IR-based approaches, and there is sufficient space for improvements.
### Rankings of Real Faulty Files
To figure out to what extent the real faulty files can be localized, we exhibit the rankings of them in the recommendation list in result/rankings. The real faulty files of quite a few bugs get top 5 rankings in the recommendation list, while some other files keep low rankings. Researchers proposed approaches to extract various contents from software engineering documents. If we use such approaches to identify the contents of issue reports, we can further improve the effectiveness of our approach.
