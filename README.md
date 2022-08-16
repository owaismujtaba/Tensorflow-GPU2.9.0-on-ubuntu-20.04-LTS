# Tensorflow-GPU2.9.0-on-ubuntu-20.04-LTS


To setup a GPU- Supportfor Nvidia and Tensor flow you need these things
1. You should have nvidia device drivers installed.
2. Check nvidia-smi it should be working.if it is not working dont worry follow the steps
![Screenshot from 2022-08-16 13-03-58](https://user-images.githubusercontent.com/45037843/184864535-2db2dbfa-8c9a-4afd-ba42-f268b975215a.png)

3. You need to downlod CUDA and cuDNN
4. Before downloading CUDA and cuDNN check for the comptability with the tensorflow version
5. ![Screenshot from 2022-08-16 13-08-05](https://user-images.githubusercontent.com/45037843/184865155-4957c2c5-361e-409e-a99e-7bfc20808f0a.png)

6. Here will be installing tensorflow 2.9.0 so we need to download CUDA 11.2 and cuDNN 8.1
7. Go to https://developer.nvidia.com/cuda-downloads then archive or directly to https://developer.nvidia.com/cuda-toolkit-archive
8. Select the version thatis 11.2 we will click on 11.2.2 which is the ist as in
9. ![Screenshot from 2022-08-16 13-15-47](https://user-images.githubusercontent.com/45037843/184866848-bfc52138-d409-430b-8161-14e090c5005f.png)


8. Select Linux then x86 then ubuntu then 20.04 then run file you will get the two steps as below
9. ![Screenshot from 2022-08-16 13-11-54](https://user-images.githubusercontent.com/45037843/184865899-4b684b90-6b95-4c98-978d-89c78873a2bd.png)
Exectute these two in your ubuntu shell. The first one will donload the file and second one for installation

