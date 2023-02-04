# To Update
1. Clone this repo:
    ```bash
    git clone https://github.com/ecriv-ai/blog-website-hugo.git
    ```
2. Get submodule content:
    ```bash
    git submodule update --init --recursive
    ```
3. Go to the `public/` folder (submodule) and make sure the `main` branch is checked out to track changes:
    ```bash
    cd public
    git checkout main
    ```
4. Make sure the `public/` submodule is up to date by pulling its latest changes and merging them in (go to parent repo first):
    ```bash
    cd ..
    git submodule update --remote --merge public
    ```
5. Now make your desired changes and build a local version of the site to see how your changes look:
    ```bash
    hugo server -D
    ```
6. Once satisfied, build the site static files:
    ```bash
    hugo -D
    ```
7. Commit and push the changes of the main repo:
    ```bash
    git add .
    git commit -m "updated site"
    git push
    ```
8. Commit and push the changes of the submodule repo:
    ```bash
    cd public
    git add .
    git commit -m "updated site"
    git push
    ```