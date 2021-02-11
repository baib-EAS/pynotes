## python download font for matplotlib in Pace-Cluster
> By Bai Bin(*1600013520@pku.edu.cn*)\
> Last updated: 2021/02/01

According to: https://blog.csdn.net/sinat_40875078/article/details/104326855
### 1.check font path
```
module load anaconda3
python
>>>import matplotlib    
>>>print(matplotlib.matplotlib_fname())
```
the output is:
```
/usr/local/pace-apps/manual/packages/anaconda3/2020.02/lib/python3.7/site-packages/matplotlib/mpl-data/matplotlibrc
```
### 2. download font
download font in this path: https://fontsnetwork.com/ and move downloaded font file to this font directory:
```
cd /usr/local/pace-apps/manual/packages/anaconda3/2020.02/lib/python3.7/site-packages/matplotlib/mpl-data/fonts/ttf
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
vi /usr/local/pace-apps/manual/packages/anaconda3/2020.02/lib/python3.7/site-packages/matplotlib/mpl-data/matplotlibrc
```
the file shows:
```
font.family         : sans-serif      
font.sans-serif     : SimHei, Bitstream Vera Sans, Lucida Grande, Verdana, Geneva, Lucid, Arial, Helvetica, Avant Garde, sans-serif  
axes.unicode_minus  : False
```
add your font at second line
### 5. restart python
