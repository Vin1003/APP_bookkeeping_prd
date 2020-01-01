# 智能记账APP——小账本

| 发布日期   | 2019.12.3    |
| ---------- | --- |
| 文件名称   | 小账本  |
| 文件现状   | 完善中    |
| 文件的主人 | 林咏妍    |
| 设计师     | 林咏妍    |
| 开发者     | 林咏妍    |
| 测试者     | 林咏妍    |

## 目标

记账APP的主要功能就是记账，但如何更方便的记账，是我们需要思考的问题。用户既可以进行文字记账，也可以进行图片记账，还可以进行语音记账，并且还能进行多货币记账，方便用户对现有财产进行理财。

## 背景和战略契合处

- 背景：现有的记账APP多种多样，网易有钱、懒得记等记账APP已占据主要市场份额，但每款记账APP的主打点都不同，用户无法在一个APP上满足多种需求，且目前无一款记账APP能进行多货币记账。

- 战略契合处：

            1.满足用户对现有花费记账的需求。

            2.采取多种方式进行记账，用户甚至连手指都不用动就可以进行记账。
 
            3.用户无法找到自己所需的记账选项时，可以通过语音记账，语音识别成文字后自动帮你分类。

            4.发票、小票等能直接进行图片记账，不需要用户进行每一笔记账。

            5.设置时间提醒用户记账，让用户自觉记账。

## 假设条件

- 用户在使用手机时：

1.首页能看到你所需要的记账方式，点击相应记账方式进行记账。

2.记账成功后，系统自动生成记账文本，以文本形式确认用户记账是否正确。

3.进入账单页面，可查看本周账单、本月账单、本季账单和年度账单。

4.账单页面显示每个记账类别所花费的金额，并且以饼状图的形式呈现出。

## 需求

| #   | 标题       | 用户故事                                                         | 重要性 | 笔记                                                                                             |
| --- | ---------- | ---------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| 1   | 语音记账   | 追星买了官咖会员，但不知道专辑的钱时算入娱乐分类还是会员充值分类 | 必须有 | 语音识别转文字后，有“会员”等字样的文字被归为会员充值类，同理可推其他分类也是采取关键字识别功能 |
| 2   | 图片记账   | 去超市买了东西，小票特别长，不想一个个进行分类记账               | 必须有 | 图片识别通过识别关键字自动帮你归类                                                               |
| 3   | 多货币记账 | 去国外旅游，明明花的是美元，却想知道自己花了多少人民币，进行记账 | 必须有 | 通过语音说出自己花了美元多少钱后，在APP内进行实时汇率的转换并进行记账                            |
| 4   | 本月账单   | 想知道这个月什么钱花得最多                                       | 必须有 | 通过饼状图能看出本月的消费结构                                                                   |


## PRD价值主张

![智能记账APP](https://images.gitee.com/uploads/images/2019/1219/002627_64d10787_1532294.png "智能记账app.png")

### PRD1 加值宣言

1.百度AI平台语音识别API进行语音识别关键字记账。

2.百度AI平台通用票据识别API进行图片记账。

3.百度AI平台货币识别API结合阿里云汇率转换API进行多货币记账。

### PRD2 核心价值

**百度AI平台**

- 短语音识别：支持普通话和略带口音的中文识别；支持粤语、四川话方言识别，支持英文识别；支持50多个领域的语义理解，如：天气，交通，娱乐等。根据语音内容理解可以将数字序列、小数、时间、分数、基础运算符正确转换为数字格式，使得识别的数字结果更符合使用习惯，直观自然；使用大规模数据集训练语言模型，根据语音的内容理解和停顿智能匹配合适的标点符号（包括，。！？），使识别结果的表现方式贴合表述，更加可懂。

- 通用票据识别：实现对各类购物小票、医疗票据、银行兑票等非标准型报销凭证的识别和录入，针对各类票据的打印方式和字体进行专项优化，对针式打印、油墨略微污损的文字提供更高的识别准确率。

- 货币识别：识别图像中的货币，以纸币为主，正反面均可准确识别，接口返回货币的名称、代码、面值、年份信息，可识别各类近代常见货币，如美元、欧元、英镑、法郎、澳大利亚元、俄罗斯卢布、日元、韩元、泰铢、印尼卢比等。

**阿里云**

- 汇率转换：提供人民币、美元、欧元、英镑、日元、韩元等100多种货币的实时汇率查询；提供汇率转换、单个货币对应的热门货币汇率行情等API。

### PRD3 核心价值于用户痛点

- **痛点一：用户需要快速知道自己手上的货币是什么货币。**

           采用货币识别，快速识别出手上的货币。

- **痛点二：用户不懂得操作记账分类。**

           采用语音识别记账，不需要动手指也能帮你自动归类。

- **痛点三：用户的小票出现非人为污损，无法进行记账。**
 
           通用票据识别API对于油墨略微污损的文字提供更高的识别准确率。

- **痛点四：用户普通话不标准，需要采用方言进行语音记帐。**

           百度短语音识别支持普通话和略带口音的中文识别；支持粤语、四川话方言识别。

### PRD4 人工智能概率性与用户痛点

- **短语音识别API:** 采用领先国际的流式端到端语音语言一体化建模方法，融合百度自然语言处理技术，近场中文普通话识别准确率达98%。

- **通用票据识别API：** 依托百度云技术实力，提供高可靠性、弹性可伸缩、高并发承载的文字识别服务，服务可用性高达99.99%。

- **货币识别API：** 基于百度深厚的深度学习和图像检索识别技术，货币识别算法业界领先，准确率高。

- **汇率转换API：** 数据更新实时，准确率能达95%以上，但是接口不太稳定，会出现返回失败的情况。

### PRD5 需求列表与人工智能API加值

**核心功能排序**

1.语音记账：通过说话进行记账，不需要用户进行过多操作。

- 短语音识别：识别用户话语中的关键字，并将其转化成文本，自动归类到所属的记账分类。

2.图片记账：通过拍摄或者上传本地图片进行记账，不需要用户重复记账。

- 通用票据识别：识别出票据中的文字，通过关键字检测将相应消费归类到所属记账分类。

3.多货币记账：将其他货币自动转换成人民币进行记账，免除用户计算汇率的烦恼。

- 货币识别：识别用户所使用的货币，方便进行记账。

- 汇率转换：实时进行汇率转换，并将结果反馈成文字到APP上，文字通过关键字识别后进行记账。与短语音识别一起使用。

## 原型

- **产品结构图**  

![产品结构图](https://images.gitee.com/uploads/images/2019/1211/042625_beca3bb1_1532294.png "产品结构图.png")

- **APP流程图**  

 ![APP流程图](https://images.gitee.com/uploads/images/2019/1211/042707_c2a72a6c_1532294.png "app流程图.png")

### 原型1 交互及界面设计

#### 记账部分

![记账部分](https://images.gitee.com/uploads/images/2020/0101/210627_a7020c31_1532294.png "index.png")

#### 账单部分

![账单部分](https://images.gitee.com/uploads/images/2020/0101/214309_5929e91b_1532294.png "账单.png")

#### 设置部分

![设置部分](https://images.gitee.com/uploads/images/2020/0101/214343_63ccbf43_1532294.png "设置.png")

### 原型2 信息设计



### 原型3 原型文档

http://yongyan.me/APP_bookeeping_axure/

备用链接： http://lyy171013051.gitee.io/bookkeeping_app_prototype

### 原型4 口头操作说明

在进入APP首页后，用户可自由选择记账方式，语音记账只需按住指定键说话即可，语音识别后会弹出文本框让用户进行确认，确认无误即可自动归类。图片记账则需用户拍下手中的票据，票据上的文字会被自动识别，自动归类。文字记账则需用户自行寻找记账分类进行记账。用户可在“我的账单”进行账单查看，进入账户信息可自定义主题，打造属于你自己的记账APP。

## API产品使用关键AI或机器学习之API的输出入展示

### API1 使用水平

- 短语音识别API：语音识别[示例Demo代码]( https://github.com/Baidu-AIP/speech-demo)

```
import sys
import json
import base64
import time

IS_PY3 = sys.version_info.major == 3

if IS_PY3:
    from urllib.request import urlopen
    from urllib.request import Request
    from urllib.error import URLError
    from urllib.parse import urlencode
    timer = time.perf_counter
else:
    from urllib2 import urlopen
    from urllib2 import Request
    from urllib2 import URLError
    from urllib import urlencode
    if sys.platform == "win32":
        timer = time.clock
    else:
        # On most other platforms the best timer is time.time()
        timer = time.time

API_KEY = 'kVcnfD9iW2XVZSMaLMrtLYIz'
SECRET_KEY = 'O9o1O213UgG5LFn0bDGNtoRN3VWl2du6'

# 需要识别的文件
AUDIO_FILE = './audio/16k.pcm'  # 只支持 pcm/wav/amr 格式，极速版额外支持m4a 格式
# 文件格式
FORMAT = AUDIO_FILE[-3:]  # 文件后缀只支持 pcm/wav/amr 格式，极速版额外支持m4a 格式

CUID = '123456PYTHON'
# 采样率
RATE = 16000  # 固定值

# 普通版

DEV_PID = 1536  # 1537 表示识别普通话，使用输入法模型。1536表示识别普通话，使用搜索模型。根据文档填写PID，选择语言及识别模型
ASR_URL = 'http://vop.baidu.com/server_api'
SCOPE = 'audio_voice_assistant_get'  # 有此scope表示有asr能力，没有请在网页里勾选，非常旧的应用可能没有

#测试自训练平台需要打开以下信息， 自训练平台模型上线后，您会看见 第二步：“”获取专属模型参数pid:8001，modelid:1234”，按照这个信息获取 dev_pid=8001，lm_id=1234
# DEV_PID = 8001 ;   
# LM_ID = 1234 ;
```

- 通用票据识别API:识别小票和发票[接口说明](https://ai.baidu.com/ai-doc/OCR/3k3h7yeqa)

```
""" 读取图片 """
def get_file_content(filePath):
    with open(filePath, 'rb') as fp:
        return fp.read()

image = get_file_content('example.jpg')

""" 调用通用文字识别, 图片参数为本地图片 """
client.basicGeneral(image);

""" 如果有可选参数 """
options = {}
options["language_type"] = "CHN_ENG"
options["detect_direction"] = "true"
options["detect_language"] = "true"
options["probability"] = "true"

""" 带参数调用通用文字识别, 图片参数为本地图片 """
client.basicGeneral(image, options)

url = "https//www.x.com/sample.jpg"

""" 调用通用文字识别, 图片参数为远程url图片 """
client.basicGeneralUrl(url);

""" 如果有可选参数 """
options = {}
options["language_type"] = "CHN_ENG"
options["detect_direction"] = "true"
options["detect_language"] = "true"
options["probability"] = "true"

""" 带参数调用通用文字识别, 图片参数为远程url图片 """
client.basicGeneralUrl(url, options)
```

- 货币识别API：识别货币[接口说明](https://ai.baidu.com/ai-doc/IMAGERECOGNITION/4k3bcxj1m)

```
""" 读取图片 """
def get_file_content(filePath):
    with open(filePath, 'rb') as fp:
        return fp.read()

image = get_file_content('example.jpg')

""" 调用通用物体识别 """
client.advancedGeneral(image);

""" 如果有可选参数 """
options = {}
options["baike_num"] = 5

""" 带参数调用通用物体识别 """
client.advancedGeneral(image, options)
```

- 汇率转换：实时转换汇率，方便进行人民币记账

```
import urllib, urllib2, sys
import ssl


host = 'https://jisuhuilv.market.alicloudapi.com'
path = '/exchange/convert'
method = 'GET'
appcode = '你自己的AppCode'
querys = 'amount=10&from=CNY&to=USD'
bodys = {}
url = host + path + '?' + querys

request = urllib2.Request(url)
request.add_header('Authorization', 'APPCODE ' + appcode)
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE
response = urllib2.urlopen(request, context=ctx)
content = response.read()
if (content):
    print(content)
```

### API2 使用分析比较

- 百度AI平台的语音识别、图像识别分类都比较仔细，能够精准针对功能进行细分，满足记账类APP只识别短语音和票据的需求。

- 目前能对票据进行分析的只有百度AI平台，并且百度AI平台还有发票识别、行驶单识别、混合票据识别等多种功能，但考虑到APP的大众性和识别图像的多样性，因此不选择一一调用票据类API，而是采用精确度相对没那么高但能识别多种票据的通用票据识别API。

- 汇率转换API目前市场上较为少见，我也仅发现有人在阿里云社区上发布汇率转换的API文档，非阿里云官方文档。

### API3 使用后风险报告

- 阿里云的汇率转换API接口不稳定，会出现返回失败的情况，需要用户进行多次尝试。

- 尝试通用票据识别API，发现一旦图片比例过小，图片内的字肉眼在电脑屏幕上看不清时，识别会出现失误。因此对于过小或者过长的票据，用户需要放大拍照或者分成多次拍照。

### API4 加分项

目前市面上无一款记账类APP拥有多货币记账功能，多货币记账功能运用了货币识别API和汇率转换API，是本产品的主打功能。

