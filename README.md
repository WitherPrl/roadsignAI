# RoadSignAI

 This road sign AI can classify images of diffrent road signs.

![A classified crossing](https://i.imgur.com/V1RqhRw.jpg)

## The Algorithm


This project utilized Jetson Nano. The model employed was a retrained resnet18, which was trained on various road signs. Each road sign in the dataset was labeled with its corresponding sign category. It utilizes the imagenet.py script with the trained model to identify the road sign category from an inputted image.

## Running this project

1. Please [download the resnet18.onnx model](https://drive.google.com/file/d/1Il6buXnDNaFhrWSfiAwaGWNTvkjdjhfw/view?usp=sharing) and labels.txt from git hub.

2. Clone the jetson-inference project from GitHub by executing the command "git clone --recursive https://github.com/dusty-nv/jetson-inference" and navigate to the respective directory.

3. Install the required Python packages by running "sudo apt-get install libpython3-dev python3-numpy".

4. Optionally dowload the test folder for images to test.

5. To classify an image, execute the following command: "imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $IMAGE $OUTPUT". Replace $NET with the folder path where the resnet18.onnx file is stored, $DATASET with the folder path where the labels.txt file is located, $IMAGE with the image file you want to classify, and $OUTPUT with the desired output file name.

[After you have completed step 1 and 2 this is a video explanation of step 3](https://youtu.be/N_9viqFRQf4)
