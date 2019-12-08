## 智能算法第二周测试题
---
### 1. 问题一：
**任务主题：**

实现自动测试评分系统。

**任务描述：**

实现自动生成10道数值随机的100以内随机加减乘除题目，每道题10分，共计100分，答题者进行回答。若答题者回答正确，继续回答下一道题并获得相应的分数（10分）
。若答题者回答错误，则再给一次机会重做该题，若再一次回答的结果正确，则获得该题目一半的分数（5分），若再一次回答的结果错误，则继续回答下一道题，不获得分数。所有题目回答完成以后生成对应答题情况、获得分数、对应评级。

**注：**

(1) 总体流程：

![总体流程](https://i.loli.net/2019/12/08/rARdBNLwqCtEeoi.jpg)

(2) 题目回答流程：

![题目回答流程](https://i.loli.net/2019/12/08/sn8XREwud3aKfSg.jpg)

**任务要求：**
(1) 使用函数式编程，注意书写主函数接口，并且主函数接口下只能出现函数的调用。
(2) 注意函数之间的参数交流方式。
(3) 答题结果包括：

* 正确和错误题目序号
* 正确率和错误率
* 每道题目答题所用时间（单位：s）

(4) 自行设计评级区间。
(5) 适当优化文字交互界面，提高使用体验。


**代码示例**
```
"""
实现自动分数评级系统
problem1v3
增加了“判断用户输入的是否为数字，若不是数字则重新输入”的功能，避免程序报错，提升用户使用体验。
"""
import random  # 引入随机模块random module.
import time  # 引入时间模块time module.
# (查询模块列表https://blog.csdn.net/xufive/article/details/102676755?utm_source=app)

i = 0
score = 0
totalscore = 0
order = 1
rate = 0
times = 1
correct = []  # 创建正确题目序号的空列表。
error = []  # 创建错误题目序号的空列表。
everytime = []  # 创建每道题目答题所用时间的空列表。


def Second_Chance():  # 定义Second_Chance()函数。
    global result
    global score
    global rate
    global add_correct
    global add_error   # 创建全局变量，以便在函数中修改。
    print("再来一次吧！")
    print(question)
    raw_loop_answer = input("请输入您的答案：")  # 获取用户输入的数字。
    while True:  # 判断用户输入的是否为数字，若不是数字则重新输入。
        if raw_loop_answer.isdigit():
            loop_answer = float(raw_loop_answer)
            break
        elif raw_loop_answer.replace(".", "").isdigit():
            loop_answer = float(raw_loop_answer)
            break
        elif raw_loop_answer.replace("-", "").isdigit():
            loop_answer = float(raw_loop_answer)
            break
        else:
            raw_loop_answer = input("您输入的不是数字，请重新输入：")
    if "+" == str(random_operator):
        if loop_answer == m + n:
            score += 5  # 第二次答对分数加5。
            rate += 10  # 第二次答对正确率加10%。
            print("回答正确！")
            # 在回答正确的空列表correct中添加此题序号order。
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            add_error = error.append(order)  # 在回答错误的空列表error中添加此题序号order。
    elif "-" == str(random_operator):
        if loop_answer == m - n:
            score += 5
            rate += 10
            print("回答正确！")
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            add_error = error.append(order)
    elif "*" == str(random_operator):
        if loop_answer == m * n:
            score += 5
            rate += 10
            print("回答正确！")
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            add_error = error.append(order)
    elif "/" == str(random_operator):
        if loop_answer == m / n:
            score += 5
            rate += 10
            print("回答正确！")
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            add_error = error.append(order)
    else:
        print("Error")


while i < 10:  # while循环，重复10次。
    score = 0
    m = random.randint(0, 100)
    n = random.randint(0, 100)
    operator = ["+", "-", "*", "/"]
    random_operator = random.choice(operator)
    result = str(m) + random_operator + str(n)
    print("第 %d 题" % (order))  # 在每一次重复前写明题号。
    question = "{} {} {}".format(m, random_operator, n)
    print(question)
    etime1 = time.time()  # 获取打印题目后时间戳。
    raw_answer = input("请输入您的答案：")
    while True:  # 判断用户输入的是否为数字，若不是数字则重新输入。
        if raw_answer.isdigit():
            answer = float(raw_answer)
            break
        elif raw_answer.replace(".", "").isdigit():
            answer = float(raw_answer)
            break
        elif raw_answer.replace("-", "").isdigit():
            answer = float(raw_answer)
            break
        else:
            raw_answer = input("您输入的不是数字，请重新输入：")
    etime2 = time.time()  # 获取用户输入后时间戳。
    # 在答题用时的空列表中添加每道题目答题所用时间（即两时间戳之差）。
    add_everytime = everytime.append(int(etime2 - etime1))
    if "+" == str(random_operator):
        if answer == m + n:
            score += 10  # 第二次答对分数加10。
            rate += 10  # 第二次答对正确率加10%。
            print("回答正确！")
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            Second_Chance()
    elif "-" == str(random_operator):
        if answer == m - n:
            score += 10
            rate += 10
            print("回答正确！")
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            Second_Chance()
    elif "*" == str(random_operator):
        if answer == m * n:
            score += 10
            rate += 10
            print("回答正确！")
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            Second_Chance()
    elif "/" == str(random_operator):
        if answer == m / n:
            score += 10
            print("回答正确！")
            rate += 10
            add_correct = correct.append(order)
        else:
            print("回答错误！")
            Second_Chance()
    else:
        print("Error")
    totalscore = totalscore + score
    print("您的目前分数：", totalscore, "分")
    i += 1
    order += 1

if 90 <= totalscore <= 100:
    print("分数评级为：A")  # 设计评级区间，打印分数评级。
elif 80 <= totalscore < 90:
    print("分数评级为：B")
elif 70 <= totalscore < 80:
    print("分数评级为：C")
elif 60 <= totalscore < 70:
    print("分数评级为：D")
elif 0 <= totalscore < 60:
    print("分数评级为：E")
else:
    print("Error")

for i in range(len(correct) - 1):
    correct.insert(i + i + 1, ",")
order_correct = "".join(str(m) for m in correct)  # 将列表correct中的中括号【】去掉。

for i in range(len(error) - 1):
    error.insert(i + i + 1, ",")
order_error = "".join(str(m) for m in error)  # 将列表correct中的中括号【】去掉。
print("正确题目序号:", order_correct, ";""错误题目序号:", order_error)  # 打印正确和错误题目序号。
print("正确率是：", rate, "%", ";""错误率是：", 100 - rate, "%",)  # 打印正确率与错误率。

for n in everytime:
    print("第", times, "题用时：", n, "s")  # 打印每道题目答题所用时间。
    times += 1
```

