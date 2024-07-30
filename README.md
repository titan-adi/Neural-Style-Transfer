# Neural-Style-Transfer
Neural Style Transfer
This project implements Neural Style Transfer using TensorFlow and TensorFlow Hub. The idea is to take two images—a content image and a style image—and blend them so that the output image looks like the content image painted in the style of the style image.

Overview
Neural Style Transfer is a technique for generating images that combine the content of one image with the style of another image. This project uses a pre-trained VGG19 network and an image stylization model from TensorFlow Hub to perform the style transfer.

Installation
To run this project, you need to have Python 3.x installed along with the following packages:

TensorFlow
TensorFlow Hub
NumPy
Pillow
Matplotlib
You can install the required packages using the following command:

bash
Copy code
pip install tensorflow tensorflow-hub numpy pillow matplotlib
Usage
Prepare Images:

Place your content and style images in the project directory.
Update the paths content_path and style_path in the script to point to your images.
Run the Script:

bash
Copy code
python style_transfer.py
This script will display the content and style images, apply the style transfer, and display the resulting stylized image.

Example
python
Copy code
content_path = 'content.jpg'
style_path = 'style.jpg'

# Load images
content_image = load_img(content_path)
style_image = load_img(style_path)

# Display images
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
imshow(content_image, 'Content Image')

plt.subplot(1, 2, 2)
imshow(style_image, 'Style Image')

plt.show()

# Apply style transfer
stylized_image = apply_style_transfer(content_image, style_image)

# Display results
plt.figure(figsize=(10, 5))
plt.subplot(1, 3, 1)
imshow(content_image, 'Content Image')

plt.subplot(1, 3, 2)
imshow(style_image, 'Style Image')

plt.subplot(1, 3, 3)
imshow(stylized_image, 'Stylized Image')

plt.show()
Project Structure
style_transfer.py: The main script containing the implementation of the style transfer.
content.jpg: The content image.
style.jpg: The style image.
Acknowledgments
This project utilizes the VGG19 model for feature extraction, which is pre-trained on the ImageNet dataset.
The style transfer model is based on the Magenta Arbitrary Image Stylization model from TensorFlow Hub.
License
This project is licensed under the MIT License.

Contributions
Feel free to contribute to this project by opening issues or submitting pull requests.

