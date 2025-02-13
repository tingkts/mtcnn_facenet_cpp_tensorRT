[Face Recognition on Jetson Nano using TensorRT | by Niclas Wesemann | Towards Data Science](https://towardsdatascience.com/face-recognition-using-tensorrt-on-jetson-nano-set-up-in-less-than-5min-7c00bf730085)

["mtcnn_facenet_cpp_tensorRT"](./mtcnn_facenet_cpp_tensorRT/) was forked from [nwesem/mtcnn_facenet_cpp_tensorRT](https://github.com/nwesem/mtcnn_facenet_cpp_tensorRT)

</br>

Concatenated projects :

|                     |                  |                                                                                                 |                                                                         |
| ------------------- | ---------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| MTCNN               | Face Detection   | [PKUZHOU/MTCNN_FaceDetection_TensorRT](https://github.com/PKUZHOU/MTCNN_FaceDetection_TensorRT) | MTCNN C++ implementation with NVIDIA TensorRT Inference accelerator SDK |
| FaceNet             | Face Recognition | [apollo-time/facenet](https://github.com/apollo-time/facenet)                                   | Tensorflow implementation of the FaceNet face recognizer                |
| TensorRT UFF plugin | .pb → .uff       | [r7vme/tensorrt_l2norm_helper](https://github.com/r7vme/tensorrt_l2norm_helper)                 | TensorRT plugin that allows to use tf.nn.l2_normalize                   |




</br>

Model transfer to TensorRT：

|         |                       |
| ------- | --------------------- |
| MTCNN   | [.pb](./mtcnn_facenet_cpp_tensorRT/facenet.pb) → [.uff](./mtcnn_facenet_cpp_tensorRT/facenetModels/facenet.uff) → [.engine](./mtcnn_facenet_cpp_tensorRT/facenetModels/facenet.engine)  |
| FaceNet | [.caffemodel](./mtcnn_facenet_cpp_tensorRT/mtCNNModels/det1_relu.caffemodel) → [.engine](./mtcnn_facenet_cpp_tensorRT/mtCNNModels/det1_relu1.engine) |



</br>


Confirmed it's able to demo on [Jetson Nano Jetpack 4.5.1](https://developer.nvidia.com/jetpack-sdk-451-archive)

 <img src="./Nano JP4.5 - jtop INFO.PNG" width = "80%" height = "80%" alt="jtop INFO"  />
