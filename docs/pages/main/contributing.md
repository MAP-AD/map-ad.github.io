---
layout: main
title: Contributing
---

Thank you for adding documentation for your tool! Here are some guidelines to get started adding documentation. We only accept documentation for tools used/developed by the MAP project.

## What should be included in the documentation

Any contributions should not be designed to replace the primary documentation of comprehensive tools. Insead, they should primarily focus on practical user guides covering installation, in/outputs, parameters and templates for running them. High-level overviews of the methodological backing of the tool are also appreciated to improve understanding.

## How to Contribute

1. **Fork the Repository**: Create a fork of the repository on GitHub
    
    <img src="/assets/img/fork.jpg" width="500px" alt="Fork demo" />  

2. **Clone the Forked Repository**: Clone your fork to your local machine.

    1. Click on the green "Code" button on your forked repository
    2. Copy the URL
    3. Open a terminal and run the following command, replacing `url_of_your_fork` with the URL you copied

    ```sh
    git clone url_of_your_fork
    ```

    <img src="/assets/img/clone.jpg" width="500px" alt="Clone demo" />

3. **Make Changes**: Add documentation

    1. Create a folder in /docs/docs/ with the name of your tool
    2. Create a new markdown (.md) file in the folder
    3. Copy and fill in the template from /docs/docs/_TEMPLATE/doc_template.md
    4. Add images to the same folder and link them in the markdown file

4. **Add and Commit Changes**: Commit your changes with a clear and concise commit message

    ```sh
    git add -A && git commit -m "description of changes"
    ```

5. **Push Changes**: Push your changes to your fork on GitHub

    ```sh
    git push
    ```

6. **Create a Pull Request**: Open a pull request to the main repository. Provide a detailed description of your changes

    1. Go to your forked repository on GitHub
    2. Click on "Contribute" and then "Open Pull Request"
    3. Add a title and description for your pull request
    4. Click "Create Pull Request"

    <img src="/assets/img/PR.jpg" width="500px" alt="Pull request demo" />  