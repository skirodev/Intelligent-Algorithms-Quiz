## 智能算法第一周测试题
### 1. 问题一：
现在有一些原始数据，其中包含两个列表，第一个列表是歌手名称，第二个列表是歌曲名
称，每首歌的歌曲名称与歌手名称一一对应（即： 原始数据中第一个列表中的第一个元素
对应第二个列表中的第二个数据）。按照下列要求，完成相应任务：

**原始数据：**

**歌手名称：**

[b'\xe5\x90\xb4\xe9\x9d\x92\xe5\xb3\xb0', 
b'\xe5\x8d\x8a\xe9\x98\xb3', 
b'Corki', b'\xe8\x8a\xb1\xe7\xb2\xa5', 
b'\xe9\x99\x88\xe6\x9f\xaf\xe5\xae\x87', b'\xe8\x8a\xb1\xe7\xb2\xa5', 
b'\xe8\x8c\x84\xe5\xad\x90\xe8\x9b\x8b', 
b'G.E.M.\xe9\x82\x93\xe7\xb4\xab\xe6\xa3\x8b', 
b'\xe5\xbc\xa0\xe7\xb4\xab\xe8\xb1\xaa', b'\xe9\x83\xad\xe9\xa1\xb6', 
b'\xe6\x9d\x8e\xe8\x8d\xa3\xe6\xb5\xa9', 
b'\xe4\xb9\xb0\xe8\xbe\xa3\xe6\xa4\x92\xe4\xb9\x9f\xe7\x94\xa8\xe5\x8
8\xb8', b'\xe4\xba\x8e\xe6\x9e\x9c', 
b'\xe9\x99\x88\xe9\x9b\xaa\xe5\x87\x9d', 
b'\xe8\xa7\xa3\xe5\xbf\xa7\xe9\x82\xb5\xe5\xb8\x85', 
b'\xe5\xa5\x87\xe7\x84\xb6', b'\xe7\x8e\x8b\xe8\xb4\xb0\xe6\xb5\xaa', 
b'Ayo97', b'\xe6\x9e\x97\xe4\xbf\x8a\xe5\x91\x88', 
b'\xe5\xbc\xa0\xe5\xad\xa6\xe5\x8f\x8b', b'\xe8\x8a\xb1\xe7\xb2\xa5', 
b'\xe6\xaf\x9b\xe4\xb8\x8d\xe6\x98\x93', 
b'\xe7\xb1\xb3\xe6\xb4\xa5\xe7\x8e\x84\xe5\xb8\xab', 
b'\xe5\xb1\x95\xe5\xb1\x95\xe4\xb8\x8e\xe7\xbd\x97\xe7\xbd\x97', 
b'\xe9\x9f\xa9\xe7\xba\xa2', b'SHAUN', b'\xe5\xa4\xa7\xe6\xb3\xab', b'Far 
East Movement', b'\xe6\x9c\xa8\xe5\xb0\x8f\xe9\x9b\x85', 
b'\xe9\x9a\x94\xe5\xa3\x81\xe8\x80\x81\xe6\xa8\x8a']
 
 **歌曲名称：**

['/起/&风///了', '一&曲//相&思 @/', '/下&/坠&Fa?lling#', '?%@出%#山@', 
'//&生#?僻字@', '@!?盗!%将#行', '浪@子!回&@#?头', '%?%!光年之&外&', '/?可
不可@以&@/', '%水&%星@&/记', '!/年&@少/有为!', '起风了&%###&', '&侧
脸?///@', '%?假装///#', '写%给&黄#淮&?/', '琵琶@行/??&!', '%往后余生/&##!', 
'感/!!谢你曾来/过@%', '%#??东西??', '@!烦#恼?#歌?', '/??离家最近的%%/路', '/不
&/%染//', '?@L@e%mon%@', '沙%##漠骆@/驼?', '飞!云!&/&之下&', 'W/%ay 
Back !H/ome/!', '//@静%/悄悄/', '!Blosso@ms//&/', '/@/可%能否/!', '#!我!
曾%#?']

**将歌手名称列表转化成对应的中英文字符串组成的列表后输出。**

**例如：**

[ ' 吴青峰' ,' 半阳' ,' Cor ki ' ,' 花粥' ,' 陈柯宇' ,' 花粥' ,' 茄子蛋' ,' G. E. M. 邓
紫棋' ,' 张紫豪' ,' 郭顶' ,' 李荣浩' ,' 买辣椒也用券' ,' 于果' ,' 陈雪凝' ,' 解忧邵
帅' ,' 奇然' ,' 王 贰浪 ' ,' Ayo97' ,' 林俊呈' ,' 张学友' ,' 花粥' ,' 毛不易' ,' 米
津玄師' ,' 展展与罗罗' ,' 韩红'，' SHAUN' ,' 大泫' ,' FarEastMovement ' ,' 木
小雅' ,' 隔壁老樊' ]

**将歌曲名称列表转成无脏字符字符串组成且每首歌曲名称添加书名号“《》”的列 表并输出。**
 
 **例如：**

[ ' 《起风了》' ,' 《一曲相思》' ,' 《下坠 Fal l i ng》' ,' 《出山》' ,' 《生僻
字》' ,' 《盗将行》' ,' 《浪子回头》' ,' 《光年之外》' ,' 《可不可以》' ,' 《水
星记》' ,' 《年少有为》' ,' 《起风了》' ,' 《侧脸》' ,' 《假装》' ,' 《写给黄淮》
' ,' 《琵琶行》 ' ,' 《往后余生》' ,' 《感谢你曾来过》' ,' 《东西》' ,' 《烦恼歌》
' ,' 《离家最近的 路》' ,' 《不染》' ,' 《Lemon》' ,' 《沙漠骆驼》' ,' 《飞云之
下》' ,' 《WayBack Home》' ,' 《静悄悄》' ,' 《Bl oss oms 》' ,' 《可能否》
' ,' 《我曾》' ]

**将歌曲名称列表转成由字符串中“ABCDE”中随机某个字符插入到每个歌曲名称随 机位置的
脏字符串组成的列表，并输出。**

**例如：**

[ ' 《B 起风了》CEBBD' ,' 《一曲相思 EABD》DE' ,' A《下坠 EFEal Cl i nEAg》
' ,' DA《B 出 DEE 山》' ,' 《E 生 EE 僻字 E》BB' ,' DE《DB 盗将 D 行》B' ,' C
《BB 浪 AE 子回头 E》' ,' C《DB 光 E 年之外 D》E' ,' 《BEE 可不可 A 以》
CE' ,' C《CEED 水星记 B》' ,' D《年 E 少 AC 有为》EB' ,' 《DE 起 D 风了 B》
DE' ,' EB《A 侧 D 脸》AE' ,' 《CD 假装 B》CBC' ,' C《写 EA 给黄淮 C》BB' ,' 
《琵 A 琶 C 行 EEBB》' ,' 《BB 往 BE 后余生》EC' ,' B《感谢你曾来过 CEA》
AE' ,' 《B 东 E 西 BBBE》' ,' DC《烦 EE 恼 EA 歌》' ,' 《离家最 CC 近的 B 路》
EBD' ,' 《不 A 染 EA》EBE' ,' C《LAeEBmon》EE' ,' 《B 沙 E 漠骆 CAE 驼》
C' ,' 《DE 飞 D 云 E 之下 E》A' ,' 《WEayEBEacAkDEHome》' ,' CC《静悄悄
B》EEA' ,' 《BEl oEAEsAsomAs》' ,' E《C 可能否 D》ACE' ,' 《A 我 EB 曾 C》
BA' ]

**利用修改后的数据自己设置一个歌曲信息查询系统，可以由歌曲名称搜索到对应的歌手
名称，也可由歌手名称搜索到对应的歌曲名称，并设置退出功能、输入检查功能，无查询结
果功能。**

**例如：**

欢迎使用歌曲信息查询系统~

请输入您需要查询 的歌手名称（歌曲名称）：郭顶

歌曲名称：《水 星记》

是否退出（y/ n）？n

请输入您需要查询的歌手名称（歌曲名称）：《水星记》

歌手名称：郭顶

是否退出（y/ n）？y

谢谢使用~

----------

**代码示例**
```
import re # 引入正则表达式re module.
import random # 引入随机random module.

beta = [b'\xe5\x90\xb4\xe9\x9d\x92\xe5\xb3\xb0', b'\xe5\x8d\x8a\xe9\x98\xb3',b'Corki',b'\xe8\x8a\xb1\xe7\xb2\xa5',
b'\xe9\x99\x88\xe6\x9f\xaf\xe5\xae\x87', b'\xe8\x8a\xb1\xe7\xb2\xa5', b'\xe8\x8c\x84\xe5\xad\x90\xe8\x9b\x8b',
b'G.E.M.\xe9\x82\x93\xe7\xb4\xab\xe6\xa3\x8b', b'\xe5\xbc\xa0\xe7\xb4\xab\xe8\xb1\xaa',
b'\xe9\x83\xad\xe9\xa1\xb6', b'\xe6\x9d\x8e\xe8\x8d\xa3\xe6\xb5\xa9',
b'\xe4\xb9\xb0\xe8\xbe\xa3\xe6\xa4\x92\xe4\xb9\x9f\xe7\x94\xa8\xe5\x88\xb8', b'\xe4\xba\x8e\xe6\x9e\x9c',b'\xe9\x99\x88\xe9\x9b\xaa\xe5\x87\x9d', b'\xe8\xa7\xa3\xe5\xbf\xa7\xe9\x82\xb5\xe5\xb8\x85',b'\xe5\xa5\x87\xe7\x84\xb6', b'\xe7\x8e\x8b\xe8\xb4\xb0\xe6\xb5\xaa', b'Ayo97',b'\xe6\x9e\x97\xe4\xbf\x8a\xe5\x91\x88', b'\xe5\xbc\xa0\xe5\xad\xa6\xe5\x8f\x8b',
b'\xe8\x8a\xb1\xe7\xb2\xa5', b'\xe6\xaf\x9b\xe4\xb8\x8d\xe6\x98\x93',
b'\xe7\xb1\xb3\xe6\xb4\xa5\xe7\x8e\x84\xe5\xb8\xab',
b'\xe5\xb1\x95\xe5\xb1\x95\xe4\xb8\x8e\xe7\xbd\x97\xe7\xbd\x97', b'\xe9\x9f\xa9\xe7\xba\xa2', b'SHAUN',
b'\xe5\xa4\xa7\xe6\xb3\xab', b'Far East Movement', b'\xe6\x9c\xa8\xe5\xb0\x8f\xe9\x9b\x85',
b'\xe9\x9a\x94\xe5\xa3\x81\xe8\x80\x81\xe6\xa8\x8a']
singer = beta[:]
for i in range(len(beta)):
    singer[i] = beta[i].decode("utf-8") 
    # 将原始数据解码（decode）转为utf-8编码格式（查询网络资料,可以通过第三方模块chardet先进行编码检测得到编码类型）。
print("") # 将不同任务结果在输出中用空行分隔开。
print("将歌手名称列表转化成对应的中英文字符串组成的列表后输出：")
print(singer) # 将歌手名称列表转化成对应的中英文字符串组成的列表后输出。



alpha = ['/起/&风///了', '一&曲//相&思 @/', '/下&/坠&Fa?lling#', '?%@出%#山@', '//&生#?僻字@', '@!?盗!%将#行', '浪@子!回&@#?头', '%?%!光年之&外&',
 '/?可不可@以&@/', '%水&%星@&/记', '!/年&@少/有为!', '起风了&%###&', '&侧脸?///@', '%?假装///#', '写%给&黄#淮&?/', '琵琶@行/??&!', '%往后余生/&##!',
  '感/!!谢你曾来/过@%', '%#??东西??', '@!烦#恼?#歌?', '/??离家最近的%%/路', '/不&/%染//', '?@L@e%mon%@', '沙%##漠骆@/驼?', '飞!云!&/&之下&',
   'W/%ay Back !H/ome/!', '//@静%/悄悄/', '!Blosso@ms//&/', '/@/可%能否/!', '#!我!曾%#?']
song = alpha[:]
random_song = song[:]
m = "《"
n = "》"
for i in range(len(alpha)):
    b = str(alpha[i])
    e = m + b + n
    x = random.randint(0,len(e))
    result = str(random.choice("ABCDE")) + e[0 : x] + str(random.choice("ABCDE")) + e[x : 2 * x] + str(random.choice("ABCDE")) + e[2 * x : 3 * x] + str(random.choice("ABCDE")) + e[3 * x : 4 * x] + str(random.choice("ABCDE")) + e[4 * x : len(e)] + str(random.choice("ABCDE")) # 字符串的切片与拼接。
    song[i] = re.sub("[/,&,#,?,@,%,!]","",e)
    random_song[i] = re.sub("[/,&,#,?,@,%,!]","",result) # 利用正则表达式过滤指定字符re.sub()（查询网络资料得到内置函数）。
print("") # 将不同任务结果在输出中用空行分隔开。
print("将歌曲名称列表转成无脏字符字符串组成且每首歌曲名称添加书名号“《》”的列表并输出：")
print(song) # 将歌曲名称列表转成无脏字符字符串组成且每首歌曲名称添加书名号“《》”的列表并输出。



print("")
print("将歌曲名称列表转成由字符串中“ABCDE”中随机某个字符插入到某个歌曲名称随机位置的脏字符串组成的列表，并输出：")
print(random_song) # 将歌曲名称列表转成由字符串中“ABCDE”中随机某个字符插入到某个歌曲名称随机位置的脏字符串组成的列表，并输出。



print("") # 将不同任务结果在输出中用空行分隔开。
print("欢迎使用歌曲信息查询系统~")
temp = input("请输入您需要查询的歌手名称（歌曲名称）：")
while(True):
    if temp in list(singer):
        order = singer.index(temp)
        print("歌曲名称：",song[int(order)])
    elif temp in list(song):
        order = song.index(temp) # 得到索引值index value.
        print("歌手名称：",singer[int(order)]) # 将song与singer索引值匹配并输出。
    else:
        print("无查询结果")
    in_content = input("是否退出？[y/n]")
    if in_content == "n":
        temp = input("请输入您需要查询的歌手名称（歌曲名称）：")
    elif in_content == "y":
        print("谢谢使用~")
        break # 终止当前循环。
```

