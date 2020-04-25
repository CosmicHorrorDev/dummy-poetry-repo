## Dummy Poetry Repo

This is just a repo for me to test out different automation changes without having it pollute my libraries history.

### TODO

* [ ] Github Actions (All 3 major platforms & multiple python versions)
    * [ ] On Push / Pull request
        * [ ] Install poetry 
            * poetry has a recommended way for this that I want to try
            * Note: This would be nice to cache since this seems particularly slow on Windows and can take up a majority of testing time for small libraries. However, this is difficult to do with not being able to extend the cache action currently
        * [ ] Install dependencies
            * Note: Most actions do this with no venv by default which I don't like since it violates isolating away the dependencies
            * Can cache this easily if `poetry.lock` is in the repo which is recommended by `poetry`
        * [ ] Lint with flake8
        * [ ] Format with black
        * [ ] Test with pytest
    * [ ] On Release
        * [ ] Still do test/lint/format dance
        * [ ] Share cache with Push / Pull Request so that next push / pull request is faster
        * [ ] Automatically build and push to pypi (can do this by storing a key for the repo in a github secret)
        * [ ] Automatically publish files to release page since some people like that I guess
* [ ] Have docs in repo with some nice orgization
* [ ] Be nice to contributors
    * [ ] Add license
    * [ ] Add pull request template
    * [ ] Add contributing guidelines
    * [ ] Add in issue templates
