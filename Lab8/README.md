# Lab 8 #
For Lab 8, I am learning about Data Analysis. The first part of this lab requires me to install a bunch of python packages. So I open Ubuntu, which I already
have installed and tried creating a virtual environemnt, although it did not work for me, so I just proceeded with installing the desired packages:
```
sudo pip3 install numpy scipy scikit-learn matplotlib pandas tensorflow keras
[sudo] password for cespejo:
Collecting numpy
  Downloading numpy-1.24.3-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (17.3 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 17.3/17.3 MB 4.1 MB/s eta 0:00:00
Collecting scipy
  Downloading scipy-1.10.1-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (34.4 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 34.4/34.4 MB 4.1 MB/s eta 0:00:00
Collecting scikit-learn
  Downloading scikit_learn-1.2.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (9.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 9.6/9.6 MB 4.4 MB/s eta 0:00:00
Collecting matplotlib
  Downloading matplotlib-3.7.1-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (11.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 11.6/11.6 MB 4.5 MB/s eta 0:00:00
Collecting pandas
  Downloading pandas-2.0.1-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (12.3 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.3/12.3 MB 4.5 MB/s eta 0:00:00
Collecting tensorflow
  Downloading tensorflow-2.12.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (585.9 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 585.9/585.9 MB 1.6 MB/s eta 0:00:00
Collecting keras
  Downloading keras-2.12.0-py2.py3-none-any.whl (1.7 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.7/1.7 MB 4.3 MB/s eta 0:00:00
Collecting threadpoolctl>=2.0.0
  Downloading threadpoolctl-3.1.0-py3-none-any.whl (14 kB)
Collecting joblib>=1.1.1
  Downloading joblib-1.2.0-py3-none-any.whl (297 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 298.0/298.0 KB 4.6 MB/s eta 0:00:00
Collecting kiwisolver>=1.0.1
  Downloading kiwisolver-1.4.4-cp310-cp310-manylinux_2_12_x86_64.manylinux2010_x86_64.whl (1.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.6/1.6 MB 3.0 MB/s eta 0:00:00
Collecting packaging>=20.0
  Downloading packaging-23.1-py3-none-any.whl (48 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 48.9/48.9 KB 334.4 kB/s eta 0:00:00
Collecting cycler>=0.10
  Downloading cycler-0.11.0-py3-none-any.whl (6.4 kB)
Collecting contourpy>=1.0.1
  Downloading contourpy-1.0.7-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (300 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 300.3/300.3 KB 2.9 MB/s eta 0:00:00
Collecting pillow>=6.2.0
  Downloading Pillow-9.5.0-cp310-cp310-manylinux_2_28_x86_64.whl (3.4 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.4/3.4 MB 4.6 MB/s eta 0:00:00
Requirement already satisfied: pyparsing>=2.3.1 in /usr/lib/python3/dist-packages (from matplotlib) (2.4.7)
Collecting python-dateutil>=2.7
  Downloading python_dateutil-2.8.2-py2.py3-none-any.whl (247 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 247.7/247.7 KB 1.8 MB/s eta 0:00:00
Collecting fonttools>=4.22.0
  Downloading fonttools-4.39.3-py3-none-any.whl (1.0 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.0/1.0 MB 4.2 MB/s eta 0:00:00
Collecting tzdata>=2022.1
  Downloading tzdata-2023.3-py2.py3-none-any.whl (341 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 341.8/341.8 KB 3.2 MB/s eta 0:00:00
Requirement already satisfied: pytz>=2020.1 in /usr/local/lib/python3.10/dist-packages (from pandas) (2022.7.1)
Collecting typing-extensions>=3.6.6
  Downloading typing_extensions-4.5.0-py3-none-any.whl (27 kB)
Requirement already satisfied: setuptools in /usr/lib/python3/dist-packages (from tensorflow) (59.6.0)
Collecting h5py>=2.9.0
  Downloading h5py-3.8.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (4.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.6/4.6 MB 4.6 MB/s eta 0:00:00
Collecting jax>=0.3.15
  Downloading jax-0.4.8.tar.gz (1.2 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 4.0 MB/s eta 0:00:00
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting flatbuffers>=2.0
  Downloading flatbuffers-23.3.3-py2.py3-none-any.whl (26 kB)
Collecting astunparse>=1.6.0
  Downloading astunparse-1.6.3-py2.py3-none-any.whl (12 kB)
Collecting protobuf!=4.21.0,!=4.21.1,!=4.21.2,!=4.21.3,!=4.21.4,!=4.21.5,<5.0.0dev,>=3.20.3
  Downloading protobuf-4.22.3-cp37-abi3-manylinux2014_x86_64.whl (302 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 302.4/302.4 KB 3.8 MB/s eta 0:00:00
Collecting tensorflow-estimator<2.13,>=2.12.0
  Downloading tensorflow_estimator-2.12.0-py2.py3-none-any.whl (440 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 440.7/440.7 KB 4.1 MB/s eta 0:00:00
Collecting gast<=0.4.0,>=0.2.1
  Downloading gast-0.4.0-py3-none-any.whl (9.8 kB)
Collecting libclang>=13.0.0
  Downloading libclang-16.0.0-py2.py3-none-manylinux2010_x86_64.whl (22.9 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 22.9/22.9 MB 2.2 MB/s eta 0:00:00
Collecting opt-einsum>=2.3.2
  Downloading opt_einsum-3.3.0-py3-none-any.whl (65 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 65.5/65.5 KB 2.4 MB/s eta 0:00:00
Collecting termcolor>=1.1.0
  Downloading termcolor-2.3.0-py3-none-any.whl (6.9 kB)
Collecting numpy
  Downloading numpy-1.23.5-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (17.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 17.1/17.1 MB 1.8 MB/s eta 0:00:00
Requirement already satisfied: six>=1.12.0 in /usr/lib/python3/dist-packages (from tensorflow) (1.16.0)
Collecting tensorboard<2.13,>=2.12
  Downloading tensorboard-2.12.3-py3-none-any.whl (5.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.6/5.6 MB 2.3 MB/s eta 0:00:00
Collecting grpcio<2.0,>=1.24.3
  Downloading grpcio-1.54.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (5.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.1/5.1 MB 2.3 MB/s eta 0:00:00
Collecting tensorflow-io-gcs-filesystem>=0.23.1
  Downloading tensorflow_io_gcs_filesystem-0.32.0-cp310-cp310-manylinux_2_12_x86_64.manylinux2010_x86_64.whl (2.4 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.4/2.4 MB 937.7 kB/s eta 0:00:00
Collecting google-pasta>=0.1.1
  Downloading google_pasta-0.2.0-py3-none-any.whl (57 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 57.5/57.5 KB 252.9 kB/s eta 0:00:00
Collecting wrapt<1.15,>=1.11.0
  Downloading wrapt-1.14.1-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (77 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 77.9/77.9 KB 2.9 MB/s eta 0:00:00
Collecting absl-py>=1.0.0
  Downloading absl_py-1.4.0-py3-none-any.whl (126 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 126.5/126.5 KB 4.1 MB/s eta 0:00:00
Requirement already satisfied: wheel<1.0,>=0.23.0 in /usr/lib/python3/dist-packages (from astunparse>=1.6.0->tensorflow) (0.37.1)
Collecting ml-dtypes>=0.0.3
  Downloading ml_dtypes-0.1.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (190 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 190.6/190.6 KB 4.6 MB/s eta 0:00:00
Collecting markdown>=2.6.8
  Downloading Markdown-3.4.3-py3-none-any.whl (93 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 93.9/93.9 KB 4.0 MB/s eta 0:00:00
Collecting google-auth-oauthlib<1.1,>=0.5
  Downloading google_auth_oauthlib-1.0.0-py2.py3-none-any.whl (18 kB)
Collecting tensorboard-data-server<0.8.0,>=0.7.0
  Downloading tensorboard_data_server-0.7.0-py3-none-manylinux2014_x86_64.whl (6.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 6.6/6.6 MB 4.9 MB/s eta 0:00:00
Collecting requests<3,>=2.21.0
  Downloading requests-2.29.0-py3-none-any.whl (62 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 62.5/62.5 KB 2.3 MB/s eta 0:00:00
Collecting werkzeug>=1.0.1
  Downloading Werkzeug-2.3.3-py3-none-any.whl (242 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 242.3/242.3 KB 4.8 MB/s eta 0:00:00
Collecting google-auth<3,>=1.6.3
  Downloading google_auth-2.17.3-py2.py3-none-any.whl (178 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 178.2/178.2 KB 2.3 MB/s eta 0:00:00
Collecting rsa<5,>=3.1.4
  Downloading rsa-4.9-py3-none-any.whl (34 kB)
Collecting cachetools<6.0,>=2.0.0
  Downloading cachetools-5.3.0-py3-none-any.whl (9.3 kB)
Collecting pyasn1-modules>=0.2.1
  Downloading pyasn1_modules-0.3.0-py2.py3-none-any.whl (181 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 181.3/181.3 KB 4.3 MB/s eta 0:00:00
Collecting requests-oauthlib>=0.7.0
  Downloading requests_oauthlib-1.3.1-py2.py3-none-any.whl (23 kB)
Collecting charset-normalizer<4,>=2
  Downloading charset_normalizer-3.1.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (199 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 199.3/199.3 KB 3.4 MB/s eta 0:00:00
Collecting idna<4,>=2.5
  Downloading idna-3.4-py3-none-any.whl (61 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 61.5/61.5 KB 1.9 MB/s eta 0:00:00
Collecting certifi>=2017.4.17
  Downloading certifi-2022.12.7-py3-none-any.whl (155 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 155.3/155.3 KB 2.3 MB/s eta 0:00:00
Collecting urllib3<1.27,>=1.21.1
  Downloading urllib3-1.26.15-py2.py3-none-any.whl (140 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 140.9/140.9 KB 4.0 MB/s eta 0:00:00
Collecting MarkupSafe>=2.1.1
  Downloading MarkupSafe-2.1.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (25 kB)
Collecting pyasn1<0.6.0,>=0.4.6
  Downloading pyasn1-0.5.0-py2.py3-none-any.whl (83 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 83.9/83.9 KB 3.1 MB/s eta 0:00:00
Requirement already satisfied: oauthlib>=3.0.0 in /usr/lib/python3/dist-packages (from requests-oauthlib>=0.7.0->google-auth-oauthlib<1.1,>=0.5->tensorboard<2.13,>=2.12->tensorflow) (3.2.0)
Building wheels for collected packages: jax
  Building wheel for jax (pyproject.toml) ... done
  Created wheel for jax: filename=jax-0.4.8-py3-none-any.whl size=1439693 sha256=2179214de26d17735ed4720bfa0891a5269f54fd572bd554f573df5825eefa96
  Stored in directory: /root/.cache/pip/wheels/09/6f/35/a8fac8b61de8e0d9eb07988481528898561923e260b1fa7d2f
Successfully built jax
Installing collected packages: libclang, flatbuffers, wrapt, urllib3, tzdata, typing-extensions, threadpoolctl, termcolor, tensorflow-io-gcs-filesystem, tensorflow-estimator, tensorboard-data-server, python-dateutil, pyasn1, protobuf, pillow, packaging, numpy, MarkupSafe, markdown, kiwisolver, keras, joblib, idna, grpcio, google-pasta, gast, fonttools, cycler, charset-normalizer, certifi, cachetools, astunparse, absl-py, werkzeug, scipy, rsa, requests, pyasn1-modules, pandas, opt-einsum, ml-dtypes, h5py, contourpy, scikit-learn, requests-oauthlib, matplotlib, jax, google-auth, google-auth-oauthlib, tensorboard, tensorflow
Successfully installed MarkupSafe-2.1.2 absl-py-1.4.0 astunparse-1.6.3 cachetools-5.3.0 certifi-2022.12.7 charset-normalizer-3.1.0 contourpy-1.0.7 cycler-0.11.0 flatbuffers-23.3.3 fonttools-4.39.3 gast-0.4.0 google-auth-2.17.3 google-auth-oauthlib-1.0.0 google-pasta-0.2.0 grpcio-1.54.0 h5py-3.8.0 idna-3.4 jax-0.4.8 joblib-1.2.0 keras-2.12.0 kiwisolver-1.4.4 libclang-16.0.0 markdown-3.4.3 matplotlib-3.7.1 ml-dtypes-0.1.0 numpy-1.23.5 opt-einsum-3.3.0 packaging-23.1 pandas-2.0.1 pillow-9.5.0 protobuf-4.22.3 pyasn1-0.5.0 pyasn1-modules-0.3.0 python-dateutil-2.8.2 requests-2.29.0 requests-oauthlib-1.3.1 rsa-4.9 scikit-learn-1.2.2 scipy-1.10.1 tensorboard-2.12.3 tensorboard-data-server-0.7.0 tensorflow-2.12.0 tensorflow-estimator-2.12.0 tensorflow-io-gcs-filesystem-0.32.0 termcolor-2.3.0 threadpoolctl-3.1.0 typing-extensions-4.5.0 tzdata-2023.3 urllib3-1.26.15 werkzeug-2.3.3 wrapt-1.14.1
```
### Next, I followed the series of commands I had to follow in Python as shown below: ###
```
$ cespejo@DESKTOP-757GQA6:~$ python3
Python 3.10.6 (main, Nov 14 2022, 16:10:14) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import numpy as np
>>> a = np.arange(6)
>>> a
array([0, 1, 2, 3, 4, 5])
>>> b = np.arange(12).reshape(4, 3)
>>> b
array([[ 0,  1,  2],
       [ 3,  4,  5],
       [ 6,  7,  8],
       [ 9, 10, 11]])
>>> c = np.arange(24).reshape(2, 3, 4)
>>> c
array([[[ 0,  1,  2,  3],
        [ 4,  5,  6,  7],
        [ 8,  9, 10, 11]],

       [[12, 13, 14, 15],
        [16, 17, 18, 19],
        [20, 21, 22, 23]]])
>>> b.shape
(4, 3)
>>> b.reshape(-1)
array([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11])
>>> b.reshape(-1,1)
array([[ 0],
       [ 1],
       [ 2],
       [ 3],
       [ 4],
       [ 5],
       [ 6],
       [ 7],
       [ 8],
       [ 9],
       [10],
       [11]])
>>> b.reshape(2,-1)
array([[ 0,  1,  2,  3,  4,  5],
       [ 6,  7,  8,  9, 10, 11]])
>>> d = np.array([20, 30, 40, 50])
>>> e = np.arange(4)
>>> f = d-e
>>> f
array([20, 29, 38, 47])
>>> e** 2
array([0, 1, 4, 9])
>>> A = np.array([[1,1], [0,1]])
>>> B = np.array([[2,0], [3,4]])
>>> A* B
array([[2, 0],
       [0, 4]])
>>> A.dot(B)
array([[5, 4],
       [3, 4]])
>>> np.dot(A,B)
array([[5, 4],
       [3, 4]])
>>> g = np.ones((2, 3), dtype=int)
>>> g
array([[1, 1, 1],
       [1, 1, 1]])
>>> h = np.random.random((2,3))
>>> h
array([[0.70945296, 0.51351248, 0.15802392],
       [0.61986155, 0.31233666, 0.96485555]])
>>> g * = 3
>>> g
array([[3, 3, 3],
       [3, 3, 3]])
>>> h += g
>>> h
array([[3.70945296, 3.51351248, 3.15802392],
       [3.61986155, 3.31233666, 3.96485555]])
>>> k = np.random.random((2,3))
>>> k
array([[0.61604904, 0.03535124, 0.66131406],
       [0.3921055 , 0.9730659 , 0.66693529]])
>>> k.sum()
3.344821037839245
>>> k.min()
0.03535124042508053
>>> k.max()
0.9730659034071589
>>> m = np.arange(12).reshape(3, 4)
>>> m
array([[ 0,  1,  2,  3],
       [ 4,  5,  6,  7],
       [ 8,  9, 10, 11]])
>>> m.sum(axis = 0)
array([12, 15, 18, 21])
>>> m.min(axis = 1)
array([0, 4, 8])
>>> m.cumsum(axis = 1)
array([[ 0,  1,  3,  6],
       [ 4,  9, 15, 22],
       [ 8, 17, 27, 38]])
>>> n=np.arange(5)
>>> n
array([0, 1, 2, 3, 4])
>>> n[[1, 3, 4]] = 0
>>> n
array([0, 0, 2, 0, 0])
>>> exit()
```
### Next, after changing my directory to lesson 8 of the iot folder, I reviewed and ran some of the desired Python codes, ran the histogram, box plots, regression, and interpolation codes, and then ran the classification, cross-validation (CV), and support-vector machine (SVM) codes. I used my command prompt (within a virtual environment) instead of Ubuntu and "py" instead of "python3":### 
```
py pyplot_simple.py
```
![image](https://user-images.githubusercontent.com/91222019/236040519-2bf436bc-df54-4e69-bf1e-2a0705e180c7.png)

```
py simple_plot.py
```
![image](https://user-images.githubusercontent.com/91222019/236040841-b70e8172-e03e-4c60-9aeb-ffac14dba345.png)

```
py pyplot_formatstr.py
```
![image](https://user-images.githubusercontent.com/91222019/236040940-dd5a3250-229e-4d7c-b104-32fefbcb6e79.png)

```
py ticklabels_demo_rotation.py
```
![image](https://user-images.githubusercontent.com/91222019/236041089-e549fd24-1f7a-4666-b36e-39a76b3573a6.png)

```
py pyplot_three.py
```
![image](https://user-images.githubusercontent.com/91222019/236041639-91bae8c6-88fd-49fe-b50f-1a3a6846422f.png)

```
py histogram_demo_features.py
```
![image](https://user-images.githubusercontent.com/91222019/236041975-6b9e881e-c644-4442-af05-6ab9fb696fc5.png)

```
py plot_lda.py
```
![image](https://user-images.githubusercontent.com/91222019/236042168-bd581353-1c45-42bc-a533-46b51ef352c8.png)

### I then proceeded with the Keras and Tensorflow commands as follows: ### 
```
cespejo@DESKTOP-757GQA6:~/iot/lesson8$ python3 keras_diabetes.py
2023-05-03 15:44:23.925111: I tensorflow/tsl/cuda/cudart_stub.cc:28] Could not find cuda drivers on your machine, GPU will not be used.
2023-05-03 15:44:23.998129: I tensorflow/tsl/cuda/cudart_stub.cc:28] Could not find cuda drivers on your machine, GPU will not be used.
2023-05-03 15:44:24.000235: I tensorflow/core/platform/cpu_feature_guard.cc:182] This TensorFlow binary is optimized to use available CPU instructions in performance-critical operations.
To enable the following instructions: AVX2 FMA, in other operations, rebuild TensorFlow with the appropriate compiler flags.
2023-05-03 15:44:26.196061: W tensorflow/compiler/tf2tensorrt/utils/py_utils.cc:38] TF-TRT Warning: Could not find TensorRT
Epoch 1/150
77/77 [==============================] - 2s 3ms/step - loss: 3.2873 - accuracy: 0.5260
Epoch 2/150
77/77 [==============================] - 0s 2ms/step - loss: 1.3073 - accuracy: 0.5768
Epoch 3/150
77/77 [==============================] - 0s 2ms/step - loss: 1.0288 - accuracy: 0.6224
Epoch 4/150
77/77 [==============================] - 0s 3ms/step - loss: 0.9310 - accuracy: 0.6068
Epoch 5/150
77/77 [==============================] - 0s 3ms/step - loss: 0.8402 - accuracy: 0.6471
Epoch 6/150
77/77 [==============================] - 0s 3ms/step - loss: 0.8392 - accuracy: 0.6680
Epoch 7/150
77/77 [==============================] - 0s 2ms/step - loss: 0.7725 - accuracy: 0.6602
Epoch 8/150
77/77 [==============================] - 0s 2ms/step - loss: 0.7485 - accuracy: 0.6667
Epoch 9/150
77/77 [==============================] - 0s 3ms/step - loss: 0.7334 - accuracy: 0.6784
Epoch 10/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6952 - accuracy: 0.6849
Epoch 11/150
77/77 [==============================] - 0s 3ms/step - loss: 0.7567 - accuracy: 0.6354
Epoch 12/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6827 - accuracy: 0.6758
Epoch 13/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6742 - accuracy: 0.6758
Epoch 14/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6757 - accuracy: 0.6706
Epoch 15/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6638 - accuracy: 0.6615
Epoch 16/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6614 - accuracy: 0.6771
Epoch 17/150
77/77 [==============================] - 0s 2ms/step - loss: 0.7007 - accuracy: 0.6992
Epoch 18/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6352 - accuracy: 0.6797
Epoch 19/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6765 - accuracy: 0.6745
Epoch 20/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6516 - accuracy: 0.6823
Epoch 21/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6196 - accuracy: 0.7005
Epoch 22/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6205 - accuracy: 0.6784
Epoch 23/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6227 - accuracy: 0.6875
Epoch 24/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6272 - accuracy: 0.6953
Epoch 25/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6141 - accuracy: 0.6914
Epoch 26/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5961 - accuracy: 0.6953
Epoch 27/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6066 - accuracy: 0.6927
Epoch 28/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6069 - accuracy: 0.6927
Epoch 29/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6006 - accuracy: 0.7018
Epoch 30/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6004 - accuracy: 0.7057
Epoch 31/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5851 - accuracy: 0.7044
Epoch 32/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5851 - accuracy: 0.6979
Epoch 33/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5905 - accuracy: 0.7148
Epoch 34/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5887 - accuracy: 0.7083
Epoch 35/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5856 - accuracy: 0.7253
Epoch 36/150
77/77 [==============================] - 0s 4ms/step - loss: 0.6019 - accuracy: 0.6940
Epoch 37/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5912 - accuracy: 0.7044
Epoch 38/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6119 - accuracy: 0.6888
Epoch 39/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5710 - accuracy: 0.7083
Epoch 40/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5676 - accuracy: 0.7227
Epoch 41/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5674 - accuracy: 0.6953
Epoch 42/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5794 - accuracy: 0.6953
Epoch 43/150
77/77 [==============================] - 0s 4ms/step - loss: 0.6231 - accuracy: 0.6836
Epoch 44/150
77/77 [==============================] - 0s 4ms/step - loss: 0.6064 - accuracy: 0.6914
Epoch 45/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6065 - accuracy: 0.6875
Epoch 46/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5618 - accuracy: 0.7266
Epoch 47/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5542 - accuracy: 0.7292
Epoch 48/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5621 - accuracy: 0.7292
Epoch 49/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5494 - accuracy: 0.7396
Epoch 50/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5664 - accuracy: 0.7253
Epoch 51/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5988 - accuracy: 0.6888
Epoch 52/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5632 - accuracy: 0.7266
Epoch 53/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5533 - accuracy: 0.7279
Epoch 54/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5474 - accuracy: 0.7240
Epoch 55/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5459 - accuracy: 0.7227
Epoch 56/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5682 - accuracy: 0.7214
Epoch 57/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5474 - accuracy: 0.7122
Epoch 58/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5408 - accuracy: 0.7305
Epoch 59/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5477 - accuracy: 0.7214
Epoch 60/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5366 - accuracy: 0.7344
Epoch 61/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5613 - accuracy: 0.7188
Epoch 62/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5550 - accuracy: 0.7305
Epoch 63/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5678 - accuracy: 0.7122
Epoch 64/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5412 - accuracy: 0.7188
Epoch 65/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5898 - accuracy: 0.7318
Epoch 66/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5282 - accuracy: 0.7474
Epoch 67/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5471 - accuracy: 0.7253
Epoch 68/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5334 - accuracy: 0.7487
Epoch 69/150
77/77 [==============================] - 0s 4ms/step - loss: 0.5361 - accuracy: 0.7357
Epoch 70/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5417 - accuracy: 0.7135
Epoch 71/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5400 - accuracy: 0.7266
Epoch 72/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5298 - accuracy: 0.7279
Epoch 73/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5534 - accuracy: 0.7279
Epoch 74/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5285 - accuracy: 0.7292
Epoch 75/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5478 - accuracy: 0.7383
Epoch 76/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5303 - accuracy: 0.7461
Epoch 77/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5423 - accuracy: 0.7279
Epoch 78/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5550 - accuracy: 0.7044
Epoch 79/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5258 - accuracy: 0.7383
Epoch 80/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5281 - accuracy: 0.7344
Epoch 81/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5464 - accuracy: 0.7240
Epoch 82/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5425 - accuracy: 0.7305
Epoch 83/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5370 - accuracy: 0.7292
Epoch 84/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5175 - accuracy: 0.7422
Epoch 85/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5209 - accuracy: 0.7422
Epoch 86/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5482 - accuracy: 0.7318
Epoch 87/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5205 - accuracy: 0.7461
Epoch 88/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5461 - accuracy: 0.7266
Epoch 89/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5357 - accuracy: 0.7227
Epoch 90/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5380 - accuracy: 0.7305
Epoch 91/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5217 - accuracy: 0.7461
Epoch 92/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5268 - accuracy: 0.7396
Epoch 93/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5481 - accuracy: 0.7318
Epoch 94/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5221 - accuracy: 0.7305
Epoch 95/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5347 - accuracy: 0.7396
Epoch 96/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5171 - accuracy: 0.7500
Epoch 97/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5295 - accuracy: 0.7539
Epoch 98/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5096 - accuracy: 0.7487
Epoch 99/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5144 - accuracy: 0.7409
Epoch 100/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5205 - accuracy: 0.7318
Epoch 101/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5374 - accuracy: 0.7305
Epoch 102/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5440 - accuracy: 0.7253
Epoch 103/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5352 - accuracy: 0.7461
Epoch 104/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5284 - accuracy: 0.7474
Epoch 105/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5022 - accuracy: 0.7461
Epoch 106/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5182 - accuracy: 0.7292
Epoch 107/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5075 - accuracy: 0.7513
Epoch 108/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5067 - accuracy: 0.7422
Epoch 109/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5167 - accuracy: 0.7370
Epoch 110/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5171 - accuracy: 0.7487
Epoch 111/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5103 - accuracy: 0.7617
Epoch 112/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5050 - accuracy: 0.7552
Epoch 113/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5189 - accuracy: 0.7409
Epoch 114/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4977 - accuracy: 0.7617
Epoch 115/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5118 - accuracy: 0.7435
Epoch 116/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5079 - accuracy: 0.7682
Epoch 117/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5047 - accuracy: 0.7539
Epoch 118/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5020 - accuracy: 0.7565
Epoch 119/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5242 - accuracy: 0.7422
Epoch 120/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5092 - accuracy: 0.7344
Epoch 121/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5114 - accuracy: 0.7617
Epoch 122/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4970 - accuracy: 0.7617
Epoch 123/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4962 - accuracy: 0.7487
Epoch 124/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5018 - accuracy: 0.7500
Epoch 125/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4918 - accuracy: 0.7695
Epoch 126/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5038 - accuracy: 0.7539
Epoch 127/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5385 - accuracy: 0.7292
Epoch 128/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5147 - accuracy: 0.7552
Epoch 129/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5202 - accuracy: 0.7357
Epoch 130/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4860 - accuracy: 0.7747
Epoch 131/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4966 - accuracy: 0.7669
Epoch 132/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5029 - accuracy: 0.7539
Epoch 133/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4919 - accuracy: 0.7695
Epoch 134/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5125 - accuracy: 0.7487
Epoch 135/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4903 - accuracy: 0.7552
Epoch 136/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5024 - accuracy: 0.7695
Epoch 137/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5006 - accuracy: 0.7643
Epoch 138/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4916 - accuracy: 0.7656
Epoch 139/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4845 - accuracy: 0.7630
Epoch 140/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4878 - accuracy: 0.7617
Epoch 141/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4914 - accuracy: 0.7578
Epoch 142/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4958 - accuracy: 0.7708
Epoch 143/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4961 - accuracy: 0.7552
Epoch 144/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5050 - accuracy: 0.7409
Epoch 145/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4959 - accuracy: 0.7539
Epoch 146/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5048 - accuracy: 0.7513
Epoch 147/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4972 - accuracy: 0.7513
Epoch 148/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4946 - accuracy: 0.7539
Epoch 149/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4882 - accuracy: 0.7682
Epoch 150/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4860 - accuracy: 0.7656
24/24 [==============================] - 0s 2ms/step - loss: 0.4597 - accuracy: 0.7852

accuracy: 78.52%
24/24 [==============================] - 0s 2ms/step
[1, 0, 1, 0, 1, 0, 0, 0, 1, 0, 0, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1, 0, 1, 0, 1, 0, 0, 1, 0, 0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 0, 1, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 1, 0, 1, 1, 1, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 1, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1, 1, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 1, 1, 0, 1, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 1, 1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 1, 1, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 1, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 1, 0, 1, 0, 1, 0, 1, 0, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 1, 1, 0, 1, 0, 0, 0, 0, 1, 1, 0, 1, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1, 0, 0, 1, 1, 1, 1, 0, 0, 0, 0, 1, 0, 1, 0, 0, 0, 0, 1, 1, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 1, 0, 1, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 1, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 1, 0, 1, 0, 1, 0, 0, 0, 0]
cespejo@DESKTOP-757GQA6:~/iot/lesson8$ python3 keras_first_network.py
2023-05-03 15:45:19.570785: I tensorflow/tsl/cuda/cudart_stub.cc:28] Could not find cuda drivers on your machine, GPU will not be used.
2023-05-03 15:45:19.725009: I tensorflow/tsl/cuda/cudart_stub.cc:28] Could not find cuda drivers on your machine, GPU will not be used.
2023-05-03 15:45:19.728555: I tensorflow/core/platform/cpu_feature_guard.cc:182] This TensorFlow binary is optimized to use available CPU instructions in performance-critical operations.
To enable the following instructions: AVX2 FMA, in other operations, rebuild TensorFlow with the appropriate compiler flags.
2023-05-03 15:45:20.883142: W tensorflow/compiler/tf2tensorrt/utils/py_utils.cc:38] TF-TRT Warning: Could not find TensorRT
Epoch 1/150
77/77 [==============================] - 2s 3ms/step - loss: 7.1932 - accuracy: 0.6211
Epoch 2/150
77/77 [==============================] - 0s 3ms/step - loss: 0.8577 - accuracy: 0.5768
Epoch 3/150
77/77 [==============================] - 0s 2ms/step - loss: 0.7036 - accuracy: 0.6328
Epoch 4/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6587 - accuracy: 0.6523
Epoch 5/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6633 - accuracy: 0.6523
Epoch 6/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6572 - accuracy: 0.6576
Epoch 7/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6442 - accuracy: 0.6693
Epoch 8/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6225 - accuracy: 0.6953
Epoch 9/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6116 - accuracy: 0.7031
Epoch 10/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6764 - accuracy: 0.6589
Epoch 11/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6166 - accuracy: 0.6862
Epoch 12/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6373 - accuracy: 0.6784
Epoch 13/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6717 - accuracy: 0.6654
Epoch 14/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5996 - accuracy: 0.6901
Epoch 15/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6052 - accuracy: 0.6979
Epoch 16/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6206 - accuracy: 0.6914
Epoch 17/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6221 - accuracy: 0.6901
Epoch 18/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6051 - accuracy: 0.6849
Epoch 19/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6095 - accuracy: 0.6888
Epoch 20/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5948 - accuracy: 0.6979
Epoch 21/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6069 - accuracy: 0.6979
Epoch 22/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6430 - accuracy: 0.6797
Epoch 23/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6009 - accuracy: 0.6966
Epoch 24/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6062 - accuracy: 0.6927
Epoch 25/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5928 - accuracy: 0.7031
Epoch 26/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5985 - accuracy: 0.6966
Epoch 27/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5803 - accuracy: 0.7096
Epoch 28/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5868 - accuracy: 0.7096
Epoch 29/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5737 - accuracy: 0.7148
Epoch 30/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5968 - accuracy: 0.6862
Epoch 31/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5871 - accuracy: 0.6966
Epoch 32/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5828 - accuracy: 0.6992
Epoch 33/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5861 - accuracy: 0.7161
Epoch 34/150
77/77 [==============================] - 0s 3ms/step - loss: 0.6049 - accuracy: 0.7122
Epoch 35/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5759 - accuracy: 0.7031
Epoch 36/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5928 - accuracy: 0.6979
Epoch 37/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5967 - accuracy: 0.7083
Epoch 38/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5719 - accuracy: 0.7135
Epoch 39/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5714 - accuracy: 0.7214
Epoch 40/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5578 - accuracy: 0.7227
Epoch 41/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5654 - accuracy: 0.7148
Epoch 42/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5557 - accuracy: 0.7109
Epoch 43/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5591 - accuracy: 0.7148
Epoch 44/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5865 - accuracy: 0.7109
Epoch 45/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5664 - accuracy: 0.7188
Epoch 46/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5673 - accuracy: 0.7122
Epoch 47/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5736 - accuracy: 0.7188
Epoch 48/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5538 - accuracy: 0.7370
Epoch 49/150
77/77 [==============================] - 0s 2ms/step - loss: 0.6045 - accuracy: 0.7109
Epoch 50/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5423 - accuracy: 0.7266
Epoch 51/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5478 - accuracy: 0.7409
Epoch 52/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5440 - accuracy: 0.7174
Epoch 53/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5707 - accuracy: 0.7070
Epoch 54/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5571 - accuracy: 0.7357
Epoch 55/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5344 - accuracy: 0.7370
Epoch 56/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5597 - accuracy: 0.7318
Epoch 57/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5437 - accuracy: 0.7409
Epoch 58/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5518 - accuracy: 0.7344
Epoch 59/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5606 - accuracy: 0.7148
Epoch 60/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5769 - accuracy: 0.7122
Epoch 61/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5453 - accuracy: 0.7266
Epoch 62/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5272 - accuracy: 0.7279
Epoch 63/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5348 - accuracy: 0.7435
Epoch 64/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5546 - accuracy: 0.7318
Epoch 65/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5312 - accuracy: 0.7279
Epoch 66/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5438 - accuracy: 0.7201
Epoch 67/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5281 - accuracy: 0.7370
Epoch 68/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5399 - accuracy: 0.7214
Epoch 69/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5145 - accuracy: 0.7500
Epoch 70/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5247 - accuracy: 0.7305
Epoch 71/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5258 - accuracy: 0.7461
Epoch 72/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5390 - accuracy: 0.7279
Epoch 73/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5203 - accuracy: 0.7435
Epoch 74/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5085 - accuracy: 0.7695
Epoch 75/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5406 - accuracy: 0.7422
Epoch 76/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5338 - accuracy: 0.7240
Epoch 77/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5308 - accuracy: 0.7526
Epoch 78/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5347 - accuracy: 0.7370
Epoch 79/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5166 - accuracy: 0.7396
Epoch 80/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5140 - accuracy: 0.7474
Epoch 81/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5418 - accuracy: 0.7227
Epoch 82/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5128 - accuracy: 0.7513
Epoch 83/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5185 - accuracy: 0.7500
Epoch 84/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5297 - accuracy: 0.7383
Epoch 85/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5138 - accuracy: 0.7539
Epoch 86/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5173 - accuracy: 0.7461
Epoch 87/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5071 - accuracy: 0.7513
Epoch 88/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5136 - accuracy: 0.7565
Epoch 89/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5309 - accuracy: 0.7383
Epoch 90/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4960 - accuracy: 0.7708
Epoch 91/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5200 - accuracy: 0.7370
Epoch 92/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4970 - accuracy: 0.7526
Epoch 93/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5043 - accuracy: 0.7578
Epoch 94/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5142 - accuracy: 0.7539
Epoch 95/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5160 - accuracy: 0.7474
Epoch 96/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5079 - accuracy: 0.7526
Epoch 97/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5610 - accuracy: 0.7318
Epoch 98/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5086 - accuracy: 0.7695
Epoch 99/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5167 - accuracy: 0.7552
Epoch 100/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5136 - accuracy: 0.7513
Epoch 101/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5247 - accuracy: 0.7409
Epoch 102/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4952 - accuracy: 0.7682
Epoch 103/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5077 - accuracy: 0.7539
Epoch 104/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4989 - accuracy: 0.7708
Epoch 105/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5007 - accuracy: 0.7591
Epoch 106/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5139 - accuracy: 0.7396
Epoch 107/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4935 - accuracy: 0.7617
Epoch 108/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5102 - accuracy: 0.7578
Epoch 109/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4891 - accuracy: 0.7682
Epoch 110/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4877 - accuracy: 0.7643
Epoch 111/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5026 - accuracy: 0.7604
Epoch 112/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4900 - accuracy: 0.7578
Epoch 113/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5091 - accuracy: 0.7513
Epoch 114/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5027 - accuracy: 0.7604
Epoch 115/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4959 - accuracy: 0.7760
Epoch 116/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4905 - accuracy: 0.7578
Epoch 117/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4862 - accuracy: 0.7552
Epoch 118/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4894 - accuracy: 0.7708
Epoch 119/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4937 - accuracy: 0.7669
Epoch 120/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4832 - accuracy: 0.7760
Epoch 121/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5278 - accuracy: 0.7474
Epoch 122/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4916 - accuracy: 0.7591
Epoch 123/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4841 - accuracy: 0.7708
Epoch 124/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4883 - accuracy: 0.7721
Epoch 125/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4851 - accuracy: 0.7682
Epoch 126/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4823 - accuracy: 0.7734
Epoch 127/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5071 - accuracy: 0.7565
Epoch 128/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4775 - accuracy: 0.7721
Epoch 129/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4733 - accuracy: 0.7669
Epoch 130/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4898 - accuracy: 0.7695
Epoch 131/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4848 - accuracy: 0.7591
Epoch 132/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4780 - accuracy: 0.7721
Epoch 133/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4825 - accuracy: 0.7734
Epoch 134/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4887 - accuracy: 0.7604
Epoch 135/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4756 - accuracy: 0.7747
Epoch 136/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4853 - accuracy: 0.7786
Epoch 137/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4796 - accuracy: 0.7747
Epoch 138/150
77/77 [==============================] - 0s 3ms/step - loss: 0.5104 - accuracy: 0.7669
Epoch 139/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5186 - accuracy: 0.7565
Epoch 140/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4722 - accuracy: 0.7773
Epoch 141/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4953 - accuracy: 0.7669
Epoch 142/150
77/77 [==============================] - 0s 2ms/step - loss: 0.5006 - accuracy: 0.7487
Epoch 143/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4837 - accuracy: 0.7786
Epoch 144/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4718 - accuracy: 0.7826
Epoch 145/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4975 - accuracy: 0.7617
Epoch 146/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4684 - accuracy: 0.7773
Epoch 147/150
77/77 [==============================] - 0s 3ms/step - loss: 0.4890 - accuracy: 0.7630
Epoch 148/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4816 - accuracy: 0.7682
Epoch 149/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4701 - accuracy: 0.7786
Epoch 150/150
77/77 [==============================] - 0s 2ms/step - loss: 0.4740 - accuracy: 0.7695
24/24 [==============================] - 0s 2ms/step - loss: 0.4634 - accuracy: 0.7904
Accuracy: 79.04
```

### Next, I made a demo folder and copied the desired Titanic files from the iot directory into the demo folder and ran the following code on my command prompt: ###

```
(env) C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\Lab8\demo>py titanic_1.py
Data Columns:
Index(['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp',
       'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked'],
      dtype='object')
Survived:
Sex
female    0.742038
male      0.188908
Name: Survived, dtype: float64
```
![image](https://user-images.githubusercontent.com/91222019/236043057-9aa89326-9cb4-4272-a524-d1e6fcf74b37.png)

```
(env) C:\Users\cesar\OneDrive - stevens.edu\Spring 2023 (3rd Year)\EE-322 D6\Lab8\demo>py titanic_2.py
Survived:
Sex     Pclass
female  1         0.968085
        2         0.921053
        3         0.500000
male    1         0.368852
        2         0.157407
        3         0.135447
Name: Survived, dtype: float64
Number of Missing Fare: 1
Indices of Missing Fare: 152
Survived:
Sex     Pclass  Fare_Bracket
female  1       2               0.833333
                3               0.977273
        2       1               0.914286
                2               0.900000
                3               1.000000
        3       0               0.593750
                1               0.581395
                2               0.333333
                3               0.125000
male    1       0               0.000000
                2               0.400000
                3               0.383721
        2       0               0.000000
                1               0.158730
                2               0.160000
                3               0.214286
        3       0               0.111538
                1               0.236842
                2               0.125000
                3               0.240000
Name: Survived, dtype: float64
```

### For part B of the lab, I started with copying the desired files into a separate "demo2" folder and going into the plt_final.py file, using nano to change up the contents of the code to what was desired:###
### I then changed all instances of "Temperature C" to "Memory Available GB" since when I did Lab 7, I measured that available memory rather than the temperature. This resulted in the following 6 graphs: ###
![image](https://user-images.githubusercontent.com/91222019/236048544-d9b17346-f57f-4c38-af31-610a69130258.png)

![image](https://user-images.githubusercontent.com/91222019/236048590-45c075cb-14dd-419d-b376-0b226cf77f32.png)

![image](https://user-images.githubusercontent.com/91222019/236048631-278c1fc4-f9fa-4a52-ad05-8313309dfd8c.png)

![image](https://user-images.githubusercontent.com/91222019/236048713-0a6f3c91-dc1d-42b2-89fb-6b4d5f451c63.png)

![image](https://user-images.githubusercontent.com/91222019/236048921-3b7eca3a-0b36-4958-8c86-cce1dfc7c1b0.png)

![image](https://user-images.githubusercontent.com/91222019/236048963-fdfd62cc-fe8e-4372-b526-7d7b7022054b.png)
