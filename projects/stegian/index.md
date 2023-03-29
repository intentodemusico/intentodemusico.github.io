## Stegian V2

**Project context:** The steganography is a branch of cybersecurity, focused on embedding hidden messages into plain images. The embedded message could vary from simple text to remote code execution scripts, making it a big threat to cybersecurity. It is impossible to determine by eye inspection whether or not an image is altered, this leading to the possibility of compromising the companies' technological infrastructure. The proposed solution helps to prevent the possible attacks by determining if an image contains or not a steganographic payload. 

**Project goals:** The goal of this project is to develop an algorithm using convolutional neural networks to detect LSB steganography in color digital images. Steganography is a branch of cybersecurity that embeds hidden messages in plain images, posing a significant threat to cybersecurity as it is difficult to detect by eye inspection. The proposed solution aims to prevent possible attacks by automating the detection process of LSB steganography.

**Solution design:** The proposed solution involves the development of a Deep Learning-based algorithm for detecting LSB steganography in color digital images. The solution begins with the collection of color digital images from various sources and preprocessing them through techniques such as image normalization, resizing, and augmentation to generate a dataset for the training and testing of the algorithm. The algorithm is then designed to implement convolutional neural networks, taking into account the characteristics of the input and output data identified in the literature review. Implementation is carried out using a suitable Deep Learning framework and programming language. Validation of the algorithm's performance in detecting LSB steganography is conducted using appropriate metrics and validation methods inherent to Deep Learning, with testing done on the generated dataset. The iterative improvement process is employed to analyze the results of testing and validation and identify areas for improvement in the algorithm's design and implementation, iterating through steps 3-5 until the desired level of performance is achieved.

**Results:** ANN and CNN models for detecting embedding artifacts on color images.


**Conclusions:**
The graduation project fulfilled all the proposed objectives, developing algorithms for LSB steganography detection in color digital images using deep learning models. In addition to completing the objectives, the project delved into additional approaches contemplated in the state of the art for steganography detection, concluding that the complexity level of the models is not always proportional to obtaining successful results, as a high level of complexity can decrease interpretability and explainability.

The ImageNet (ILSVRC) training dataset was chosen due to its labeled and balanced images with a distribution of categories considered natural and invariant in the training and testing processes of the models. For the development of projects with large datasets, it is important to estimate the required computational capacity, as deep learning modeling requires more resources than other models.

The F1 score, precision, training time, and estimation time were the performance metrics chosen for the evaluation of the deep learning model, providing a general overview of the final state of the model. The deep learning model using convolutional neural networks has a precision of 50% and an F1 score of 66%, comparable to Mamada's model. However, this performance is far from being comparable to other scenarios such as heart beat recognition (93-94%), habitat image segmentation (94-95%), and facial expression recognition (smiles) independent of the subject with face detection (97.6%).

The high temporal complexity of the model in training, low interpretability, and explainability that prevent a deepening of the improvement processes, and the nature of the steganographic procedure that modifies pixels with a different pattern than just graphics, are factors that limit the performance of deep learning models in this scenario. Despite this, deep learning models are extremely useful in scenarios where steganography detection is required, but it is important to consider the limitations and required resources.

**Recommendations:**
Usually, Deep Learning problems can be solved by simpler models, so it is recommended to carefully evaluate the cost/benefit in each project and start modeling in order of complexity (from the least complex and most interpretable to the most complex and least interpretable).

On the other hand, variations in color depth, storage, dataset structuring, and applied steganography method should be taken into account, as steganography is not usually embedded in the form of specific borders or pictorial patterns, a situation that can vary with respect to the implementation of the steganographic method. It is recommended to study the steganographic method before proposing black-box detection techniques that cannot be parameterized by their complexity.

Finally, it is suggested to structure a dataset by tuples (cover and stego) for each image in the selected sample, and store the datasets in an uncompressed format, thus avoiding alteration of the spatial transformations performed by the steganographic methods.

**Future work:** 
• Restructure the architecture of the dataset used in order to reinforce the learning achieved by the different models on the dataset. Additionally, test approaches with different formats for storing images.
• Replicate the detailed process in this project using alternative steganographic algorithms embedded in images to find results in line with the State of the Art.
• Propose a model architecture to identify the amount of payload and steganographic method present.
• Develop a Deep Learning model that not only detects the presence of steganographic payload but can also extract and decode the hidden message embedded within it.
• Utilize different Deep Learning approaches, such as adversarial neural networks and deep neural networks, to test the effectiveness of different Machine Learning methods in solving the same problem.
• Extract the weights assigned to the neurons of the Deep Learning models in their convolutional and densely connected layers to reconstruct the patterns of steganography detection.

<!--**Takeaways:** Not necesarily a larger model will make a better prediction.