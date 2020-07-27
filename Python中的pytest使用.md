### pytest 概述
* pytest 是第三方开发的一个Python测试模块， 可以编写小型测试，而且可以拓展以支持应用程序和库的复杂功能测试，帮助我们编写更好的程序

### 安装pytest

* 命令行运行 pip install -U pytest
* 检查是否安装了正确的版本   pytest --version

### 简单的测试

* 1、新建  test_sample.py

  `def inc(x): 
  
        return x + 1    
        
    def test_answer():  
    
        assert inc(3) == 5 
 `
 
* 在test_sample.py 文件的目录下，执行pytest命令， pytest 将运行当前目录及其子目录下所有名称为test_*.py  或者 *_test.py 的文件

* assert 断言 语句验证测试期望值，pytest中有一种断言反思机制，可以智能报告assert表达式的中间值

* 2、创建文件名  ：  test_001.py


`def fun(a):

    rerurn a + 1
    
 def test_001():
 
    assert fun(2) == 3
    
 def test_002():
    
    assert fun(2) == 4
    
`

* cmd 命令框输入命令   pytest test_001.py

* 执行结果， 1个成功，1个失败

* 说明： 测试文件后边的字母代表含义汇总：

-- "." 代表测试通过，

-- F(Fail) : 失败

-- E(error): 错误

-- s(skip) : 跳过

--X(xpass): 预期失败 但是成功x

--xfail : 预期失败执行也失败

### 理论部分

* 文件、 包、 类、 函数编写规则

-- 文件或（包） ： 必须以test_开头 或者以_test结尾

-- 类 ： 必须以Test 开头， 且不含有init 方法

-- 函数/方法  ： 必须以 test_开头

* 断言 方法： assert

-- assert aa : 判断aa为真

-- assert not aa : 判断aa不为真

-- assert a in b : 判断b包含a

-- assert a==b : 判断a等于b

-- assert a！=b : 判断a不等于b

-- 另外， 如果断言后有错误的，想给出友好提示，可以使用以下方式

-- assert 5 == add(4,4), "add()方法结果不等于5，而等于{0}".format(add(4,4))

* 相关使用

-- 重复执行失败用例  pip install pytest-rerunfailures

-- 使用示例 ： pytest test.py --reruns 3

-- 


