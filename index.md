## My script for installing Python TensorFlow Object Detection libs

[Python TensorFlow Object Detection installation](https://gist.github.com/zby/e3341751f54bc92ebcc1d9da08a9459a
)

It installs all the system prerequisites (like protobuf), CUDA, the python libs, and also downloads one neural network (because I worked with it).
The crucial part is this:
`pip3 install pycocotools --no-build-isolation --no-binary :all:`
Apparently there is a pip bug that makes it installing binaries for numpy 1.20.xx and then linking pycocotools with it without it:
https://stackoverflow.com/questions/66060487/valueerror-numpy-ndarray-size-changed-may-indicate-binary-incompatibility-exp/66743692#66743692

None of the online tutorials I found touched this problem. Maybe it will be fixed some day.

