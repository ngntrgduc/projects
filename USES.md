Here's my crawled repositories list, using GitHub API. 

I often find myself being lost when visiting someone's repositories. If that user has more than 100 repositories, then it will be very exhausted... So I made this to crawl repositories of GitHub users painlessly.

**PS**: I made this to view repositories of other accounts. But then I realized this can be used for personal.

### How to use?
- Install requirements:
    ```python
    pip install requests python-dotenv
    ```
- Create GitHub Token, with `repo` scope.
- Create a `.env` file, and put the token in:
    ```
    GITHUB_TOKEN = <your_token_here>    
    ```
- Run `main.py`.

If you want to ignore specific repositories: Create a `ignore.txt` file, and write the name of the repositories you want to ignore, separated by line.

For more information, visit: https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#list-repositories-for-a-user

### TODO
- [x] `Ignore` repo lists
- [x] Crawl all repositories (for users with 100+ repositories)
- [x] Starred repo crawler