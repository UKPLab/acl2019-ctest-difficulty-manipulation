# Instructions for runnning the code for generating manipulated C-tests

Please ensure to have set up python 3 and to *download* and include all necessary resources and put them into a folder named *DKPro-Core*. Additionally, ensure that *DifficultyPrediction.jar* [1] lies within the folder where the code is executed.

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

[1] https://public.ukp.informatik.tu-darmstadt.de/acl19-C_test-difficulty-manipulation/DifficultyPrediction.jar
