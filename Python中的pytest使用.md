### pytest 概述
* pytest 是第三方开发的一个Python测试模块， 可以编写小型测试，而且可以拓展以支持应用程序和库的复杂功能测试，帮助我们编写更好的程序

### 安装pytest

* 命令行运行 pip install -U pytest
* 检查是否安装了正确的版本   pytest --version

### 简单的测试

* 新建  test_sample.py

  `def inc(x): 
  
        return x + 1    
        
    def test_answer():  
    
        assert inc(3) == 5 
 `
