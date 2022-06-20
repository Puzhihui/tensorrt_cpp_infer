## 1.参数配置
    vim CMakeLists.txt

    修改USER_DIR参数为自己的用户根目录

    vim infer.cc修改如下参数

        output_name: char* output_name = (char*)"output";

        trt_model_path: 的tensorrt推理引擎（models_save目录下trt后缀的文件）

        test_img: 测试图片路径

        INPUT_W INPUT_H: 输入图片宽高

        NUM_CLASS: 训练的模型有多少类

        参数配置完毕
## 2.复制trt_engine_lib
    project目录下：
    mkdir trt_engine_lib   cd trt_engine_lib
    copy Generate_LibMyTtrEngine-trt721/bin/libMyTtrEngine-trt721.so .
    具体编译见：Generate_LibMyTtrEngine-trt721
## 3.编译
    mkdir build

    cd build

    cmake ..

    make

    ./TensorRTsEngine 

