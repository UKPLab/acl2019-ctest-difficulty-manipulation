# Manipulating the Difficulty of C-Tests
### Ji-Ung Lee, Erik Schwan, and Christian M. Meyer
#### [UKP Lab, TU Darmstadt](https://www.informatik.tu-darmstadt.de/ukp/ukp_home/index.en.jsp)

Source code and data from our user study of our [ACL 2019 article](https://www.aclweb.org/anthology/P19-1035/). 

```
@inproceedings{lee-etal-2019-manipulating,
    title = "Manipulating the Difficulty of C-Tests",
    author = "Lee, Ji-Ung and Schwan, Erik and Meyer, Christian M.",
    booktitle = "Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics",
    month = jul,
    year = "2019",
    address = "Florence, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/P19-1035",
    pages = "360--370",
}
```

> **Abstract:** We propose two novel manipulation strategies for increasing and decreasing the difficulty of C-tests automatically. This is a crucial step towards generating learner-adaptive exercises for self-directed language learning and preparing language assessment tests. To reach the desired difficulty level, we manipulate the size and the distribution of gaps based on absolute and relative gap difficulty predictions. We evaluate our approach in corpus-based experiments and in a user study with 60 participants. We find that both strategies are able to generate C-tests with the desired difficulty level.

* **Contact person:** Ji-Ung Lee, ji-ung.lee@tu-darmstadt.de
    * UKP Lab: http://www.ukp.tu-darmstadt.de/
    * TU Darmstadt: http://www.tu-darmstadt.de/

Drop me a line or report an issue if something is broken (and shouldn't be) or if you have any questions.

## Data collected in the user study

This folder contains the dataset which was collected in the user study for the human evaluation of our difficulty manipulation strategies.
All files are tab separated. The column headers describe the content and are self explanatory.

_ctests.tsv_

The generated C-tests, their ids, the gap solutions, their target difficulties and the texts in plaintext and tokenized form.
`#GAP#` indicates the removed part which is to be gapped and the ctest_type names the strategy which was used to create the C-test.

_user_ctest_mapping.tsv_

Individual user answers for each C-test. uid and cid indicate the according C-test and unique User ID.
Error-rate is the user's error rate on this particular C-test, and answers their answer for each gap.
The answers contain following information: `[gap-id]-[user-answer]`
The user feedback is contained in the column feedback and the column correct describes which answer matches with the solution.
The column score simply sums up the number of correct answers (maximum of 20).

_user_sorting.tsv_

The final sorting provided by each user (column uid). The entries in the other columns contain the IDs of the ranked C-tests.

_user_questionnaire.tsv_

The answers for each user for the self-assessment they provided at the begin of the study.


### Data Protection Disclaimer

This data was collected using a self-implemented web interface. Each participant was provided with randomly created credentials linked to a unique user ID. To protect our participants identity, the ordering during handing out the credentials was further obfuscated and randomized. We did not collect any personal information from our participants and asked each participant for their consent on publishing this dataset. For experiments with a similar setup and task, we obtained the approval of the university's ethics commission.

Please also note the license of this data:

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>

