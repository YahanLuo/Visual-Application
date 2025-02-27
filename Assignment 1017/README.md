
# Yahan Luo 1017 Assignment
<details>
<summary>Part 1：我所选取的数据集</summary>
  
## 我所选取的数据集
 * 我所选取的数据集是纽约市Airbnb的数据，它发布于两个月之前，数据评分到达10分（well documented）。数据包内部包括一份CSV文件和一张纽约市的地图。
![NY Ab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/NYAbsource.png)
* 我在八月份刚刚去纽约旅游了十天，其黄金地段高昂的酒店价格给我留下了难以磨灭的心理阴影。所以，我想用这份数据看一看，是否能用法拉盛的宾馆价格住到曼哈顿的民宿？还是说天下的乌鸦一般黑，Airbnb和hotel的价格不相上下？
* 打开 CSV文件，我发现这份文件里包含十六个变量，它们分别是：房间id、房间名、房主id、房主名、街区、街区所在片区、经度、维度、房间种类、价格、最短租赁天数、总浏览量、最近一次浏览记录、月均浏览量、每年可住天数。还有一个变量我没看懂，叫做calculated_host_listings_count。
* 整个文件包含48895条数据，毕竟纽约也是个旅游城市，拥有这么多家Airbnb也是情理之中的事情。我仗着自己电脑性能好，决定把这五万条数据都用上。
* 但很快，我就意识到了什么叫“莽夫之勇”。
</details>

<details>
 <summary>Part2：我所使用的工具以及呈现</summary>
  
## 我所使用的工具以及呈现
* 我选择的呈现工具有Tableau，数可视，镝数，BDP。
* 我原本也想用Echarts来着，但是它复杂的编辑过程吓退了我。
* 下面我将从不同类别数据的呈现的角度，整理我的呈现内容以及感想：
  
  ### 1. 所在位置
  * 这是纽约Airbnb所在的区域位置条形图；
  ![ny ab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/AirbnbLocation.png)
  * 我尝试在地图上用直观的方式标注Airbnb的位置，企图看出是否存在中心点。然而，我低估了五万个数据的力量————整个曼哈顿被密密麻麻地覆盖着，根本看不出任何的集中区域；
  ![ny ab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/NYAblocation.png)
  * 我没死心，又企图在地图上表明街区。然而，我忘记了街区本来就是一个地理元素，在地图上标注出来没有任何的作用。只得到一张花花绿绿的纽约街区地图。
  ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/NYab%20neighborhood.png)
  
   ### 2. 价格
   * 价格是呈现的重头戏，我决心用好几种方法呈现：地图散点图，热力图，地图条形图。
   * 首先，我在Tableau中做出了第一份散点图。然而效果很不理想。本来的颜色是从黄色到红色渐变，但地图上大部分点都是黄色的且分布过于密集，几乎看不出价格的差别。（就跟上面那张黄色点点差不多）我仔细回想，发现纽约Airbnb的价格区间比较特殊————
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/price%20range.png)
   * 如果将红色设置为最高价格————也就是一万美元；那么大部分Airbnb都呈现黄色的“低价”是肯定的。于是，我做出了一些调整：把红色设置为五百美元（再往上就是我住不起的地方），把点的半径调小，不透明度降低，最后得到如下的价格散点图：
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/price%201.png)
   * 下面是用BDP生成的价格热力图。
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/price%20heat.png)
   * 就在我研究热力图时，BDP同一类别下的另一个图标吸引了我————地图条形图。说实话我觉得它长得很丑且非常诡异，但是我发现这个图表竟然可以比较友好地展现之前被我牺牲掉的极高值：
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/price%20bar.png)
    
    ### 3. 房间类别
   * Airbnb的房间一般分为整套出租、单间出租和房间共享；这是整个纽约Airbnb的room type的bar图：
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/room%20type.png)
   *  这是加入neighborhood-group变量之后的bar图：
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/room%20type%20location%20bar.png)
   * 由于非常非常非常喜欢桑基图，所以这次也强行做了一张：
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/location%20type.png)
   * 然而！最喜欢的还是这张！房间类别+所在位置+价格（颜色深浅）:
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/location%20type%202.png)
   
   ### 4. 房间名字
   * 最后皮了一下，做一个房间名字的词云：
   ![nyab](https://github.com/YahanLuo/2019-Visual-Data-Journalism/blob/master/Assignment%201017/room%20name.png)

</details>

<details>
  
<summary>Part 3：我的感想</summary>

## 我的感想
  1. **关于数据：**
  * 我之前做数据新闻的时候，总是因为找不到合适的数据而无比难受。所以当五万条整齐干净的数据出现在我眼前时，我真是快乐得快要死掉。有一种饥荒者见大餐的感觉。
  * 但等冷静下来发现，我并没有很好地将这份数据用尽。大约一半的变量我都没有挖掘出里面的信息，这是正常的吗？还是我的能力太局限？
  2. **关于工具：**
  * 线上工具虽然简易快捷，但终究还是有不小的限制性，尤其是在美工方面。同时也希望老师能多介绍一些国外的线上可视化网站，看看是否有能够兼具便捷性、美观、自由度的工具。
  * 而tableau虽然好用，其美工上也较为有限。特别有特色的数据表是否都得用代码来写？或者用ps，ai？
  3. **关于做图：**
  * 最直观的数据表达方法（比方说地图）可能会比较吸引人，但未必是最好的表现方法。就像不同地区的房间价格，是否用一个盒须图能更好表达呢？既能够看出不同地区价格的平均值差异，又能够看出其极差和上下限。（我没做盒须图是因为没研究懂怎么做）
  * 做图的时候不能想当然，先研究数据的特点，再结合特点去想呈现方式。否则就可能因为不了解数据特性而出错。
  * 为了呈现出大部分数据的规律而牺牲一小部分数据（让它们呈现不出来），比如让所有五百美金以上的房间都显示出一个颜色，这样值得吗？
  * btw：做个笔记，下次试试datawrapper和infogram！
</details>


    
    
 
  
