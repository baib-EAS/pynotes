## python download font for matplotlib in Pace-Cluster
> By Bai Bin(*1600013520@pku.edu.cn*)\
> Last updated: 2021/02/01

According to: https://blog.csdn.net/sinat_40875078/article/details/104326855
### 1.check font path
```
module load anaconda3
conda activate penv (which is your python env name)
python
>>>import matplotlib    
>>>print(matplotlib.matplotlib_fname())
```
the output is:
```
/storage/home/hcoda1/1/bbai32/.conda/envs/penv/lib/python3.9/site-packages/matplotlib/mpl-data/matplotlibrc
```
### 2. download font
download font in this path: https://fontsnetwork.com/ and move downloaded font file to this font directory:
```
cd /storage/home/hcoda1/1/bbai32/.conda/envs/penv/lib/python3.9/site-packages/matplotlib/mpl-data/fonts/ttf
```

### 3. remove matplotlib buffer directory
```
>>>import matplotlib
>>>matplotlib.get_cachedir()
```
the output is:
```
/storage/home/hcoda1/1/bbai32/.cache/matplotlib
```
romove it by:
```
rm -rf /storage/home/hcoda1/1/bbai32/.cache/matplotlib
```
### 4. change matplotlibrc file
```
vi /storage/home/hcoda1/1/bbai32/.conda/envs/penv/lib/python3.9/site-packages/matplotlib/mpl-data/matplotlibrc
```
change the follow items:
```
 font.family         : sans-serif   
 # uncomment     
 font.sans-serif     : SimHei, Bitstream Vera Sans, Lucida Grande, Verdana, Geneva, Lucid, Arial, Helvetica, Avant Garde, sans-serif  
 # uncomment and add your new font after colon
 axes.unicode_minus  : False
 # uncomment and change True into False
```
### 5. restart python
