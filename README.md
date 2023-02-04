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
4. Go to the parent repo again and make the desired changes:
    ```bash
    cd ..
    ```
5. Build a local version of the site to see how your changes look:
    ```bash
    hugo server -D
    ```
6. Once satisfied, build the site static files:
    ```bash
    hugo -D
    ```
7. The add and commit the changes (from the main repo, not the submodule):
    ```bash
    git add .
    git commit -m "updated site"
    ```
8. Push changes to this repo and let changes propagate to the submodule that contains the public static site data:
    > The `--recurse-submodules=check` flag ensures that changes are pushed to the submodule correctly before pushing to the main repo.
    ```bash
    git push --recurse-submodules=check
    ```