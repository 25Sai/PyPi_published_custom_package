# PyPi_published_custom_package

This is a python package used to generate random passwords. Here, we used Modules:"String" & "Secrets" to generate a secured password which you can use anywhere.

# Below are the steps to upload your own package.

1. Make sure you have Python and pip installed on your system.

2. 2. Create your python package.

3. Create LICENCE.txt file | To see MIT License open url -
   https://opensource.org/licenses/MIT

4. Create setup.py file as below
  import setuptools
  setuptools.setup(
  name='<package_name>', 
  version='0.1',
  author="<author’s name",
  author_email="<author’s email>",
  description="<Basic desc>",
  packages=setuptools.find_packages(),
  classifiers=[
  "Programming Language :: Python :: 3",
  "License :: OSI Approved :: MIT License",
  "Operating System :: OS Independent",
  ],
 )
  
5. Test the package
  
6. Install the required packages:
   • Setuptools: Setuptools is a package development process library designed for creating and 
   distributing Python packages.
   • Wheel: The Wheel package provides a bdist_wheel command for setuptools. It creates 
   .whl file which is directly installable through the pip install command. We'll then upload 
   the same file to pypi.org.
   • Twine: The Twine package provides a secure, authenticated, and verified connection 
   between your system and PyPi over HTTPS.
   • Tqdm: This is a smart progress meter used internally by Twine.
   1) pip install setuptools wheel
   2) pip install tqdm
   3) pip install twine
  
7. Run the command to create whl file
   python setup.py bdist_wheel
  
8. Register Yourself in pypi org account.
  
9. Run the command to upload package
   twine upload --repository-url https://upload.pypi.org/legacy/ dist/*
  
10. Test the package
    Pip install <packagename>
