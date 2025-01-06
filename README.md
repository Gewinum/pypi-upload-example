# How to Upload a Project to PyPI

This guide will walk you through the steps to upload your project to PyPI (Python Package Index).

## Prerequisites

1. **Configure Two-Factor Authentication (2FA) on PyPI**

   - Log in to your PyPI account.
   - Go to your account settings.
   - Enable Two-Factor Authentication (2FA) and follow the instructions to set it up.

2. **Create a PyPI API Token**

   - After enabling 2FA, go to your PyPI account settings.
   - Under the "API tokens" section, create a new token.
   - Copy the token and store it securely. You will need it to upload your package.

## Steps to Upload Your Project

1. **Install Setuptools and Twine**

   Setuptools and Twine are utilities for building and publishing Python packages to PyPI. Install them using pip:

   ```sh
   pip install setuptools twine
   ```

2. **Build Your Package**

   Ensure your `setup.py` is correctly configured. Then, build your package:

   ```sh
   python setup.py sdist
   ```

   This will create distribution files in the `dist/` directory.

3. **Upload Your Package Using Twine**

   Use Twine to upload your package to PyPI:

   ```sh
   twine upload dist/* -u __token__ -p <your-api-token>
   ```

   Replace `<your-api-token>` with the API token you created earlier.

4. **Verify Your Upload**

   After uploading, verify that your package is available on PyPI by visiting your project's page on PyPI.

Congratulations! You have successfully uploaded your project to PyPI.