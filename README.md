## Dummy Poetry Repo

This is just a repo for me to test out different automation changes without having it pollute my libraries history.

### TODO

* [x] Github Actions (All 3 major platforms & multiple python versions)
    * [ ] On Push / Pull request
        * [x] Install poetry 
            * poetry has a recommended way for this that I want to try **(not done, was having issues with flake8 on windows that I'll have to test)**
            * Note: This would be nice to cache since this seems particularly slow on Windows and can take up a majority of testing time for small libraries. However, this is difficult to do with not being able to extend the cache action currently (I think the easiest way to handle this would be with an action that can take some functionality from tha caching action which is currently still being worked on)
        * [x] Install dependencies
            * Note: Most actions do this with no venv by default which I don't like since it violates isolating away the dependencies
            * Can cache this easily if `poetry.lock` is in the repo which is recommended by `poetry`
        * [x] Lint with flake8
        * [x] Format with black
        * [x] Test with pytest
    * [ ] On Release
        * [ ] ~~Still do test/lint/format dance~~ (do we have to though, it should already be done)
        * [ ] Share cache with Push / Pull Request so that next push / pull request is faster (nothing to share till poetry itself is cached)
        * [ ] Automatically build and push to pypi (can do this by storing a key for the repo in a github secret)
        * [ ] Automatically publish files to release page since some people like that I guess
* [ ] Have docs in repo with some nice organization
* [ ] Be nice to contributors
    * [ ] Add license
    * [ ] Add pull request template
    * [ ] Add contributing guidelines
    * [ ] Add in issue templates
