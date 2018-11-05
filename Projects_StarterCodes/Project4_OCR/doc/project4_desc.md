## STAT GR5243 Fall 2018 Applied Data Science
### Project 4 Optical Character Recognition (OCR) Post-processing Algorithms Evaluation

In this project, working in teams, you will evaluate and **compare** a pair of algorithms for **OCR Post-processing**.

#### Challenge

**OCR** is a technology that enables you to convert different types of documents, such as scanned paper documents, PDF files or images captured by a digital camera into editable and searchable data. The OCR system consists of pre-processing module, word recognition module and post-processing module, which are pipelined together to retrieve a relevant scanned document.

![image](ocr_flowchart.png)

For this project, each team is assigned **a pair of research papers** from the *OCR* literature. You will study the papers carefully and implement the algorithms, from scratch, in `R`. **Paper assignments will be posted to a piazza post specific to individual groups**. You will also receive a set of 97 text files. For each pair, you have a ground-truth text file and a *[Tesseract](https://en.wikipedia.org/wiki/Tesseract_(software))* processed file as the *input* for the task. 

#### Evaluation criteria 
- Readabiity and reproducibility of codes
- Validity of evaluation (well-defined measures of performance; experiment set up)
- Presentation and organization (report, github and in-class presentation)

*(More details will be posted as grading rubrics in courseoworks/canvas)*

#### Project details

##### Project time table.

Each week, we will give a tutorial in class and having live discussion and brainstorm sessions. The instruction team will join team discussions during class and online. 

- week 1 (Nov 7/8): Introduction and project description. An overview of OCR.
- week 2 (Nov 14/15): Q&A.
- Final presentation (Nov 28/29)

##### Suggested team workflow
1. [wk1] Week 1 is the **reading and coding** week. Read the papers assigned to you, understand the algorithms and start coding up the algorithms; Also load the data into `R` and understand its structure. 
2. [wk1] Each team is strongly recommended to demonstrate project progress by posting a project plan with task assignments as issues on GitHub by Nov 14/15. 
4. [wk1] As a team, brainstorm about your evaluation plan.  
5. [wk2] Based on the outcomes from week 1's reading and brainstorm sessions, continue coding and start evaluation. 
6. [wk2] Week 2 is the **evaluation** week. 
7. [wk2] It is ok to separate into two sub-teams, one working on one algorithm, as long as the two teams have the same criteria for evaluating the algorithms. The two sub-teams can also serve as others' validators. 
8. By using R Notebook to carry out coding and evaluation, your final report can just be adding explanation and comments to your Notebook. 

##### Working together
- Setup a GitHub project folder with everyone listed as contributor. Everyone clones the project locally and creates a local branch. 
- The team can work in subgroups of 2-3, which might meet more frequently than the entire team. However, everyone should check in regularly on group discussion online and changes in the GitHub folder.
- Learn to work together is an important learning goal of this course.   

#### Resources

##### Error Detection Papers 

1. Kulp, S., & Kontostathis, A. (2007, November). On Retrieving Legal Files: Shortening Documents and Weeding Out Garbage. In TREC. [Link](http://webpages.ursinus.edu/akontostathis/KulpKontostathisFinal.pdf)
* Rule-based techniques
* OCR Error Detection is in section 2.2

2. Riseman, E. M., & Hanson, A. R. (1974). A contextual postprocessing system for error correction using binary n-grams. IEEE Transactions on Computers, 100(5), 480-493. [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1672564&tag=1)
* Positional binary digram technique
* Error Detection is in section 3-a

3. Wudtke, R., Ringlstetter, C., & Schulz, K. U. (2011, September). Recognizing garbage in OCR output on historical documents. In Proceedings of the 2011 Joint Workshop on Multilingual OCR and Analytics for Noisy Unstructured Text Data (p. 8). ACM. [Link](https://dl.acm.org/citation.cfm?doid=2034617.2034626)
* Probabilistic techniques -- SVM garbage detection
* Features are in section 5 (you can choose not to implement ‘Levenshtein distance’ feature)

##### Error Correction Papers 

1. Riseman, E. M., & Hanson, A. R. (1974). A contextual postprocessing system for error correction using binary n-grams. IEEE Transactions on Computers, 100(5), 480-493. [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1672564&tag=1)
* Positional binary digram technique
* Error Detection is in section 3-b

2. Mei, J., Islam, A., Wu, Y., Moh'd, A., & Milios, E. E. (2016). Statistical learning for OCR text correction. arXiv preprint arXiv:1611.06950. [Link](https://arxiv.org/pdf/1611.06950.pdf)
* Supervised model -- correction regressor

3. Church, K. W., & Gale, W. A. (1991). Probability scoring for spelling correction. Statistics and Computing, 1(2), 93-103. [Link](https://link.springer.com/content/pdf/10.1007%2FBF01889984.pdf)
* Focus on section 3 -- probability scoring without context

4. Church, K. W., & Gale, W. A. (1991). Probability scoring for spelling correction. Statistics and Computing, 1(2), 93-103. [Link](https://link.springer.com/content/pdf/10.1007%2FBF01889984.pdf)
* Same paper as above one, but focus on section 5 -- probability scoring with contextual constraints

5. Wick, M., Ross, M., & Learned-Miller, E. (2007, September). Context-sensitive error correction: Using topic models to improve OCR. In Document Analysis and Recognition, 2007. ICDAR 2007. Ninth International Conference on (Vol. 2, pp. 1168-1172). IEEE. [Link](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4377099)
* Topic modeling.

##### Example starter codes

As an example, you can find in the GitHub starter codes an example using part of rule-based error detection method. 