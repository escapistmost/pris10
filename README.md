# pris10
AI课程任务10 - 基于 T5_translate 中英俄互相翻译的实现

## 使用说明
1. 创建并激活虚拟环境：
    ```bash
    conda create -n pris10 python=3.9
    conda activate pris10
    ```

2. 克隆项目并安装依赖：
    ```bash
    git clone https://github.com/escapistmost/t5trans.git
    pip install .
    ```

## 启动说明
1. 导入并启动训练和测试：
    ```python
    import pris10
    
    print("hello world 翻译为中文",t5trans.trans_en2ch('hello world'))
    print("Здравствуйте, мир 翻译为中文",t5trans.trans_ru2ch('Здравствуйте, мир'))
    print("你好，世界 翻译为俄文",t5trans.trans_ch2ru('你好，世界'))
    print("你好，世界 翻译为英文",t5trans.trans_ch2en('你好，世界'))
    print("hello world 翻译为俄文",t5trans.trans_en2ru('hello world'))
    print("Здравствуйте, мир 翻译为英文",t5trans.trans_ru2en('Здравствуйте, мир'))
    ```

## 依赖项
- Python 3.10
- Conda
- PyTorch 
- transformers
- sentencepiece

## 其它问题

这个库会自动下载模型到你运行这个代码的models文件夹中（没有这个文件夹它也会自动创建一个），但是大家可能会遇到没有魔法（翻不了墙，下半天结果网络错误），位置存储不够等问题，下面是对应的解决方法：

下面是这个模型的链接，你需要自己去把这个文件下载下来并解压到对应的地址，然后使用函数的时候增加一个参数（下面是个例子）：
https://pan.baidu.com/s/1TMbs6OGJC4daS7tqqFlLAw?pwd=ggnm

```
print(t5trans.trans_en2ch('hello world'), cache_dir='./my_model/')
```
上面对应的文件夹相对格式是这样的：

    main.py  ——你运行文件时的相对路径
    my_model ——文件夹
        models--utrobinmv--t5_translate_en_ru_zh_small_1024 ——模型文件