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
