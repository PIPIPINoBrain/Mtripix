  # Auchor
* 西安三重像素科技有限公司
* Xi'an Triple Pixel Technology Co., 
* @PIPIPINoBrain
* 联系方式：PIPIPINoBrain@163.com

### <font color='red'>Mtripix.Mutils.Mtrans(usage)</font>


#### <font color=#FF7D00>安装方式</font> 
pip install Mtripix

#### <font color=#FF7D00>使用示例</font> 
import Mtripix.Mutils.Mtrans as Mt

idxs = [1,2,3]   
labels = ["dog", "cat", "person"]   
d = Mt.labels2dict(labels, idxs)    
path_xml = "C:\\Users\\18829\\Desktop\\MTP\\A.xml"
path_txt = "C:\\Users\\18829\\Desktop\\MTP\\A1.txt"     
Mt.xml2yoloobb(path_xml, path_txt, d)   

# Environment
* json
* numpy
* Lxml


# Mtripix Function
## Mtripix.Mutils(lists)
### Mtripix.Mutils.Mtrans(lists)
* [__Mtripix.Mutils.Mtrans.labels2dict(labels, idxs)__](#font-colorff7d00mtripixmutilsmtranslabels2dictlabels-idxsfont)          **功能:  生成namedict，标签与类别对应的字典**  
* [__Mtripix.Mutils.Mtrans.voc2yolo(path_xml, path_txt, namedict)__](#font-colorff7d00mtripixmutilsmtransvoc2yolopathxml-pathtxt-namedictfont)   **功能:  labelme标注的xml格式转yolo格式(label, xc, yc, w, h)————相对值**                     
* [__Mtripix.Mutils.Mtrans.json2yolo(path_json, path_txt, namedict, mode)__](#font-colorff7d00mtripixmutilsmtransjson2yolopathjson-pathtxt-namedict-modefont) **功能:  labelimg标注的json格式转yolo检测格式(label, xc, yc, w, h)和分割格式(label, xy, xy, xy, xy)————相对值**               
* [__Mtripix.Mutils.Mtrans.voc2dotaobb(path_xml, path_txt)__](#font-colorff7d00mtripixmutilsmtransvoc2dotaobbpathxml-pathtxtfont-)**功能:  rolabelme和labelme标注的xml格式转DOTA数据格式,(xy,xy,xy,xy,label,difficulty)————绝对值**  
* [__Mtripix.Mutils.Mtrans.voc2yoloobb(path_xml, path_txt, namedict)__](#font-colorff7d00mtripixmutilsmtransvoc2yoloobbpathxml-pathtxt-namedictfont-)**功能:  rolabelme和labelme标注的xml格式转yoloobb数据格式,(label, xy, xy, xy, xy)————相对值**
* [__Mtripix.Mutils.Mtrans.yolo2voc(path_img, path_txt, path_xml, namedict)__](#font-colorff7d00mtripixmutilsmtransyolo2vocpathimg-pathtxt-pathxml-namedictfont)   功能:  转yolo格式(label, xc, yc, w, h)转labelme标注的xml格式————绝对值**   

### <font color=FF0000>Mtripix.Mutils.Mtrans(intrudction)</font>
#### <font color=#FF7D00>Mtripix.Mutils.Mtrans.labels2dict(labels, idxs)</font>
**@input:** 
  * labels(list/tuple):  标签名 里边都是str
  * idxs(list/tuple): 类别名 里边都是str 

**@return:** 
  * namedict(dict) 标签与类别对应的字典

#### <font color=#FF7D00>Mtripix.Mutils.Mtrans.voc2yolo(path_xml, path_txt, namedict)</font>
**@input:** 
  * path_xml(str):  xml文件地址
  * path_txt(str): 生成的yolo的txt地址
  * namedict(dict): 标签和类别对应的字典

**@return:** 
  * 0

#### <font color=#FF7D00>Mtripix.Mutils.Mtrans.json2yolo(path_json, path_txt, namedict, mode)</font>
**@input:** 
  * path_json(str):  json文件地址
  * path_txt(str): 生成的yolo的txt地址
  * namedict(dict): 标签和类别对应的字典
  * mode(str): 一共可填两种模式“detection”和“segmentation”, 分别对应yolo检测和分割的文件,默认是“detection”

**@return:** 
  * 0

#### <font color=#FF7D00>Mtripix.Mutils.Mtrans.voc2dotaobb(path_xml, path_txt)</font> 
**@input:** 
  * pathxml(str):  xml文件地址
  * path_txt(str): 生成的DOTA的txt地址

**@return:** 
  * 0

#### <font color=#FF7D00>Mtripix.Mutils.Mtrans.voc2yoloobb(path_xml, path_txt, namedict)</font> 
**@input:** 
  * path_xml(str):  xml文件地址
  * path_txt(str): 生成的yoloobb的txt地址
  * namedict(dict): 标签和类别对应的字典

**@return:** 
  * 0

#### <font color=#FF7D00>Mtripix.Mutils.Mtrans.yolo2voc(path_img, path_txt, path_xml, namedict)</font>
**@input:** 
  * path_img(str): 图像地址
  * path_txt(str): 图像的yolo格式txt地址
  * path_xml(str): 生成的xml地址
  * namedict(dict): 类别和标签对应的字典

**@return:** 
  * 0