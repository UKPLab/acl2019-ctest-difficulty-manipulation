# Note: This is a modified version of the code for the anonymous review process.
To comply with the anonymous review process, we cannot provide all necessary resources to run our manipulation system. Thus, all resources which are too big to be uploaded to softconf (e.g. our reproduced difficulty prediction system) will be provided upon acceptance on an external file server. 

# Instructions for runnning the code for generating manipulated C-tests

Please ensure to have set up python 3 and to *download* and include all necessary resources and put them into a folder named *DKPro-Core*. Additionally, ensure that *DifficultyPrediction.jar* lies within the folder where the code is executed.

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


The resulting C-test is in DKPro TC format, i.e. a tab separated file with a single token in each line.
Each sentence is split by a '----'. Gapped tokens include the gap id, the part of the word which is displayed, and the estimated error rate.
