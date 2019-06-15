## About DVC-CC
This branch was automated created with the tool DVC-CC. This tool connects DVC (https://dvc.org/) to CC (www.curious-containers.cc) to run your defined stages with DVC in a docker on your cloud system with CC. [More information about DVC-CC](https://github.com/deep-projects/dvc-cc)

## DVC-Status


<details><summary>Before Execution</summary>
<p>

```
WARNING: Output 'tf_models/tf_model.h5'(Stage: 'dvc/train_network.dvc') is missing version info. Cache for it will not be collected. Use dvc repro to get your pipeline up to date.
WARNING: Output 'tensorboards/tb'(Stage: 'dvc/train_network.dvc') is missing version info. Cache for it will not be collected. Use dvc repro to get your pipeline up to date.
WARNING: Output 'outputs/all-history.json'(Stage: 'dvc/train_network.dvc') is missing version info. Cache for it will not be collected. Use dvc repro to get your pipeline up to date.
WARNING: Output 'outputs/history-summary.json'(Stage: 'dvc/train_network.dvc') is missing version info. Cache for it will not be collected. Use dvc repro to get your pipeline up to date.
Preparing to collect status from ssh://annusch@avocado01.f4.htw-berlin.de/data/ldap/jonas/pcam_with_dvc_cc
[##############################] 100% Collecting information
Pipeline is up to date. Nothing to reproduce.

```

</p>
</details>




<details><summary>After Execution</summary>
<p>

```
Preparing to collect status from ssh://annusch@avocado01.f4.htw-berlin.de/data/ldap/jonas/pcam_with_dvc_cc
[##############################] 100% Collecting information
	new:                tf_models/tf_model.h5
	new:                tensorboards/tb
	new:                tensorboards/tb/plugins/profile/2019-06-15_12-52-37/local.trace
	new:                tensorboards/tb/train/events.out.tfevents.1560603154.pepper02.355.680.v2
	new:                tensorboards/tb/validation/events.out.tfevents.1560603154.pepper02.355.688.v2
	new:                outputs/all-history.json
	new:                outputs/history-summary.json

```

</p>
</details>



## How to rerun this experiment:
The following sections describe how you can rerun the dvc stages yourself.
### Pure command line (run the experiment local)
```
sh code/download_pcam_dataset.sh
python code/train.py -lr 0.0001 --num-of-preprocesses 1

```
### Using DVC (run the experiment local)
```
dvc repro -P
```
### Using CC (run the experiment on a server)
```
faice exec cc_execution_file.red.yml
```
## Executed System
The scipt ran on the following system:


<details><summary>GPU(s)</summary>
<p>

```
                          name    memory.total [MiB]
====================================================
          Tesla V100-PCIE-16GB             16130 MiB

```

</p>
</details>




<details><summary>Other Hardware</summary>
<p>

```
H/W path         Device   Class          Description
====================================================
/0/0                      memory         754GiB System memory
/0/1                      processor      Intel(R) Xeon(R) Gold 6130 CPU @ 2.10GHz
/0/2                      processor      Intel(R) Xeon(R) Gold 6130 CPU @ 2.10GHz
/0/100/1f.2               memory         Memory controller

```

</p>
</details>




<details><summary>Software</summary>
<p>

```
Package              Version             
-------------------- --------------------
absl-py              0.7.1               
appdirs              1.4.3               
asciimatics          1.11.0              
asn1crypto           0.24.0              
astor                0.8.0               
backcall             0.1.0               
bcrypt               3.1.6               
bleach               3.1.0               
certifi              2019.3.9            
cffi                 1.12.3              
chardet              3.0.4               
colorama             0.4.1               
configobj            5.0.6               
configparser         3.7.4               
contextlib2          0.5.5               
cryptography         2.7                 
cycler               0.10.0              
decorator            4.4.0               
defusedxml           0.6.0               
distro               1.4.0               
dulwich              0.19.11             
dvc                  0.41.3              
dvc-cc-agent         0.3.0               
dvc-cc-connector     0.3.0               
entrypoints          0.3                 
future               0.17.1              
gast                 0.2.2               
gitdb2               2.0.5               
GitPython            2.1.11              
google-pasta         0.1.7               
grandalf             0.6                 
grpcio               1.21.1              
h5py                 2.9.0               
humanize             0.5.1               
idna                 2.8                 
inflect              2.1.0               
ipykernel            5.1.1               
ipython              7.5.0               
ipython-genutils     0.2.0               
ipywidgets           7.4.2               
jedi                 0.13.3              
Jinja2               2.10.1              
joblib               0.13.2              
jsonpath-ng          1.4.3               
jsonschema           2.6.0               
jupyter              1.0.0               
jupyter-client       5.2.4               
jupyter-console      6.0.0               
jupyter-core         4.4.0               
Keras-Applications   1.0.8               
Keras-Preprocessing  1.0.9               
kiwisolver           1.1.0               
Markdown             3.1.1               
MarkupSafe           1.1.1               
matplotlib           3.1.0               
mistune              0.8.4               
mock                 3.0.5               
nanotime             0.5.2               
nbconvert            5.5.0               
nbformat             4.4.0               
networkx             2.3                 
notebook             5.7.8               
numpy                1.16.4              
pandas               0.24.2              
pandocfilters        1.4.2               
paramiko             2.4.2               
parso                0.4.0               
pexpect              4.7.0               
pickleshare          0.7.5               
Pillow               6.0.0               
pip                  19.1.1              
ply                  3.11                
prometheus-client    0.6.0               
prompt-toolkit       2.0.9               
protobuf             3.8.0               
ptyprocess           0.6.0               
pyasn1               0.4.5               
pycparser            2.19                
pyfiglet             0.8.post1           
Pygments             2.4.2               
pyjson               1.3.0               
PyNaCl               1.3.0               
pyparsing            2.4.0               
python-dateutil      2.8.0               
pytz                 2019.1              
pyzmq                18.0.1              
qtconsole            4.5.1               
red-connector-ssh    0.7                 
requests             2.22.0              
ruamel.yaml          0.15.96             
schema               0.7.0               
scikit-learn         0.21.2              
scipy                1.3.0               
scp                  0.13.2              
Send2Trash           1.5.0               
setuptools           40.6.2              
six                  1.12.0              
sklearn              0.0                 
smmap2               2.0.5               
tb-nightly           1.14.0a20190301     
tensorboard          1.13.1              
tensorflow-gpu       2.0.0a0             
termcolor            1.1.0               
terminado            0.8.2               
testpath             0.4.2               
tf-estimator-nightly 1.14.0.dev2019030115
tornado              6.0.2               
traitlets            4.3.2               
treelib              1.5.5               
urllib3              1.25.3              
wcwidth              0.1.7               
webencodings         0.5.1               
Werkzeug             0.15.4              
wheel                0.33.4              
widgetsnbextension   3.4.2               
zc.lockfile          1.4                 

```

</p>
</details>


