# Android-Neural-Network-Api
The Android Neural Networks API (NNAPI) is an Android C API designed for running computationally intensive operations for machine learning on mobile devices. NNAPI is designed to provide a base layer of functionality for higher-level machine learning frameworks (such as TensorFlow Lite, Caffe2, or others) that build and train neural networks. The API is available on all devices running Android 8.1 (API level 27) or higher.
# Understanding the Neural Networks API runtime
NNAPI is meant to be called by machine learning libraries, frameworks, and tools that let developers train their models off-device and deploy them on Android devices. Apps typically would not use NNAPI directly, but would instead directly use higher-level machine learning frameworks. These frameworks in turn could use NNAPI to perform hardware-accelerated inference operations on supported devices.

Based on the app’s requirements and the hardware capabilities on a device, Android’s neural networks runtime can efficiently distribute the computation workload across available on-device processors, including dedicated neural network hardware, graphics processing units (GPUs), and digital signal processors (DSPs).

For devices that lack a specialized vendor driver, the NNAPI runtime relies on optimized code to execute requests on the CPU.

The diagram below shows a high-level system architecture for NNAPI.

https://developer.android.com/ndk/images/nnapi/nnapi_architecture.png
