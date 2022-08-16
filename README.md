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
10. Exectute these two in your ubuntu shell. The first one will download the file and second one for installation. 
11. Wait for the menu to pop up and continue the type accept.
12. ![Screenshot from 2022-08-16 13-18-59](https://user-images.githubusercontent.com/45037843/184867386-d9048b5d-4454-477c-ad17-9440d38a5c68.png)
13. if your nvidia-smi was not working the check the Driver and CUDA Toolkit11.2. you do not need Samples Demo Suite and Documentation
14. ![Screenshot from 2022-08-16 13-21-50](https://user-images.githubusercontent.com/45037843/184867941-87785818-5136-4bde-bed0-bb3befa337d9.png)
15. You now have CUDA installed and now you need cuDNN 
16. Download cuDNN from this https://developer.nvidia.com/rdp/cudnn-archive
17. Select the compatible version for tensorflow2.9 we need 8.1
18. ![Screenshot from 2022-08-16 13-24-46](https://user-images.githubusercontent.com/45037843/184868404-f4d0a673-c20f-4593-96e4-050b84b170a2.png)
19. Click on the link and download the for Linux(x86_64) if you have 64. A tar file will be download
20. Unzip the tar file by thefollowing command
21. tar -xvf file_name
22. ![Screenshot from 2022-08-16 13-26-26](https://user-images.githubusercontent.com/45037843/184868700-25db635b-4517-42e3-9226-0d7b14ea6dff.png)
23. You will now have a cuda folder in created in the current directory and the files are extracted there
24. Type these three commands but remeber to check you have cuda folder in you current directory.
25. sudo cp cuda/include/cudnn*.h /usr/local/cuda/include
26. sudo cp -P cuda/lib64/libcudnn* /usr/local/cuda/lib64
27. sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*
28. open .bashrc file using nano
29. nano ~/.bashrc
30. add these two lines at the end of the file
31. export PATH=/usr/local/cuda/bin${PATH:+:${PATH}}$ 
32. export LD_LIBRARY_PATH=/usr/local/cuda/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
33. save it and close it.
34. Restart the terminal and check 
35. nvidia-smi 
36. nvcc -V
37. both shod be working
38. ![Screenshot from 2022-08-16 13-31-18](https://user-images.githubusercontent.com/45037843/184869425-a3fa8f67-98c9-4948-a451-9a13984c72be.png)

39. now create an python environment 
40. sudo apt-get install -y python3-pip
41. sudo apt-get install -y python3-venv
42. python -m venv environemnt_name
43. activate your environment
44. source environment_name/bin/activate
45. using pip install tensorflow-gpu 2.9.0
46. pip install tensorflow-gpu==2.9.0
47. now you have tensorflow-gpu2.9.0 CUDA 11.2 and cuDNN 8.1 installed
48. wile installing tensorflow-gpu you might get the error of protobuf version comptability issue
49. Solve that using
50. pip install --upgrade protobuf==3.11
51. That is all
 



