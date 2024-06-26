# Manipulating the Difficulty of C-Tests
### Ji-Ung Lee, Erik Schwan, and Christian M. Meyer
#### [UKP Lab, TU Darmstadt](https://www.informatik.tu-darmstadt.de/ukp/ukp_home/index.en.jsp)

Source code of our [ACL 2019 article](https://www.aclweb.org/anthology/P19-1035/). 

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

## Instructions for running the code for generating manipulated C-tests

The code runs under python 3. Please ensure to download *all* necessary resources (see below) and put them into a folder named `DKPro-Core`. 

Make sure to download the [DifficultyPrediction.jar](https://tudatalib.ulb.tu-darmstadt.de/bitstream/handle/tudatalib/2704/DifficultyPrediction.jar?sequence=3&isAllowed=y) and put it to the folder where the code is executed (`python_code/`).
<!--- old file location: https://public.ukp.informatik.tu-darmstadt.de/acl19-C_test-difficulty-manipulation/DifficultyPrediction.jar -->

## Setting up the resources

To set up the DKPro-Core environment properly, you require access to additional resources which we either cannot distribute freely or are too big to host them ourselves. Please request access to the following resources and put them into the specified folders:

* [TreeTagger and Chunker](https://www.cis.uni-muenchen.de/~schmid/tools/TreeTagger/) : Put the English binaries under `~/DKPro-Core/Treebank/lib/en/`
* [Web1T](https://catalog.ldc.upenn.edu/LDC2006T13) :  1gram, 2gram, and 3gram to be placed unter `~/DKPro-Core/web1t/en/`
* [Semantic analysis calculated on the Wikipedia corpus](https://tudatalib.ulb.tu-darmstadt.de/bitstream/handle/tudatalib/2704/wp_eng_lem_nc_c.zip?sequence=6&isAllowed=y) : To be extracted to `~/DKPro-Core/difficultyResources/`
<!--- old file location: https://public.ukp.informatik.tu-darmstadt.de/baer/wp_eng_lem_nc_c.zip -->

## Setting up the virtual environment and running the code

1.	Create a virtual environment, e.g. using conda: 

		conda create --name diffman

2.	Activate the environment:

		source activate diffman

3.	Set the DKPro-Core folder as the DKPRO_HOME environment:

		export DKPRO_HOME=~/DKPRO-Core

4.	Install dependencies using pip:

		pip install -r requirements.txt

5. 	Execute the code by:

		python CTestGenerator_Strategies_perFile.py [options]

Options are as follows:

--strategy : Strategy to create C-test. DEF, SIZE, or SEL

--target : Target error rate for the generated C-test. (float)

--infile : Input file with the text used to generate the C-test. 

--ctest : Output file for the C-test.

Example usage:

        python CTestGenerator_Strategies_perFile.py --strategy DEF --target 0.5 --infile data/cd10_2.txt --ctest results/cd10_2_DEF.txt

The resulting C-test is in DKPro TC format, i.e. a tab separated file with a single token in each line.
Each sentence is split by a '----'. Gapped tokens include the gap id, the part of the word which is displayed, and the estimated error rate.


### Further comments

This code reuses various resources introduced by Beinborn (2016). Please refer to the work below for more specific information on the used features. 

### References
*Beinborn, Lisa Marina*. [Predicting and Manipulating the Difficulty of Text-Completion Exercises for Language Learning](http://tuprints.ulb.tu-darmstadt.de/5647/).
Technische Universität Darmstadt, Darmstadt, Ph.D. Thesis, (2016) 
