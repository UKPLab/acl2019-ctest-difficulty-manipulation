# Manipulating the Difficulty of C-Tests
### Ji-Ung Lee, Erik Schwan, and Christian M. Meyer
#### [UKP Lab, TU Darmstadt](https://www.informatik.tu-darmstadt.de/ukp/ukp_home/index.en.jsp)

This repository contains code and data from our [ACL 2019 article](https://www.aclweb.org/anthology/P19-1035/). 
To run the code, it is necessary to first setup a respective `DKPro` environment as described in the [README](https://github.com/UKPLab/acl2019-ctest-difficulty-manipulation/tree/master/code).
All models to run the C-Test generation with both our proposed strategies are provided in the folder `python_code`.
The data from our user study is described in the respective [README](https://github.com/UKPLab/acl2019-ctest-difficulty-manipulation/tree/master/data) in the data folder.

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

For license information, please see the LICENSE and README files in `code/*` and `data/*`.

> This repository contains experimental software and is published for the sole purpose of giving additional background details on the respective publication. 

## Project structure

* `code` &mdash; Experimental source codes
* `data` &mdash; Used C-tests and participant answers from our user study

## Data description

A description of the data can be found in `data/README.md` .

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>

<!--
## Experiments

### Requirements

* Java 1.7 and higher, Maven (for Java-based experiments)
* Python 2.7 and `virtualenv` (for Python-based experiments)
    * GPU is recommended but not required
* Tested on 64-bit Linux versions
-->

