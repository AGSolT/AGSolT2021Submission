# SolAR

## Quickstart
The easiest way to try out the SolAR is to download the dynamosadocker.tar and or fuzzerdocker.tar files from <a href="https://drive.google.com/drive/folders/1qAxzToqqCNkGBWFmDPC_O03BVCLDHbDX?usp=sharing">Google drive.</a>

These can be used in conjunction with docker using the commands:

```
docker load < fuzzerdocker.tar
docker load < dynamosadocker.tar

docker run -it fuzzer:1.2.0
docker run -it dynamosa:1.2.0
```

The file structure in the docker image is the same as the <a href="https://github.com/AGSolT/SolAR/tree/master/DynaMOSA">DynaMOSA</a> and <a href="https://github.com/AGSolT/SolAR/tree/master/Fuzzer">Fuzzer</a> folders in this git repository. To generate tests for a smart contract, simply copy the relevant smart contract folder from the SmartContracts/RWContracts folder to the SmartContracts/BatchContracts folder and run:

```
./Generate_Tests.sh
```

The configuration options for SolAR can be changed in the <a href="https://github.com/AGSolT/SolAR/blob/master/DynaMOSA/SolMOSA/Config.ini"> Config.ini</a> file. And the relevant options to be changed can be found either in table 3 of the paper, or by quickly looking at the <a href="https://github.com/AGSolT/SolAR/blob/master/Tracklist">Tracklist</a>.

## Running Locally
If you want to download the tool and play with the code locally, simply:

1. Download the code in this repository.
2. Set up and activate an [environment](https://docs.python.org/3/tutorial/venv.html) with python 3.7 (e.g., following [these](https://stackoverflow.com/questions/70422866/how-to-create-a-venv-with-a-different-python-version) instructions). Newer versions of python will be tested in the future.
3. Navigate to the folder you downloaded in step 1 and install the required python packages by running `pip install -r requirements.txt`.
4. You're ready to go! Follow the instructions below to start testing.
