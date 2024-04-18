## Get-Info-GitHub

### Why?
I often find myself being lost when visiting someone's repositories/stars. If that user has more than 100 repositories/stars, then it will be very exhausted. So I made this to crawl all of it.

### Features
- Get all repositories, starred, gists
- Crawled result to a folder if needed (Default will crawl to `data/<github-username>/`)
- Ignore specific repositories in `ignore.txt`

### How to use?
- Install requirements:
    ```python
    pip install requests python-dotenv fire
    ```
- Create GitHub Token, with `repo` scope
- Create a `.env` file, and put the token in:
    ```
    GITHUB_TOKEN = <your_token_here>    
    ```
- If you want to ignore specific repositories: Create a `ignore.txt` file, and write the name of the repositories you want to ignore, separated by line.
- For basic crawling:: 
```python
python main.py <github_username>
```
- If the user has more than 100 repositories/starred/gists, you must pass flag `-a` or `--all` to get all of its:
```python
python main.py <github_username> -a
```

- If you want the crawled results in a folder, pass `-f` or `--folder`:
```python
python main.py <github_username> -f
```

For more information, visit: https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#list-repositories-for-a-user
