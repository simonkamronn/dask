There are a variety of other projects related to dask that are often
co-released.  We may want to check their status while releasing


Release per project:

*   Tag commit

        git tag -a x.x.x -m 'Version x.x.x'

*   and push to github

        git push dask master --tags

*  Upload to PyPI

        git clean -xfd
        python setup.py sdist bdist_wheel --universal
        twine upload dist/*

*   Update conda recipe feedstock on `conda-forge <https://conda-forge.github.io/>`_.
    *  Update conda-smithy and run conda-smithy rerender
    *  Get sha256 hash from pypi.org
    *  Update version number and hash in recipe
