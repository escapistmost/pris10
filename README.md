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