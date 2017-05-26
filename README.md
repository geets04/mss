My sCool Server Documentation
-----------------------------
Checkout http://mss-doc.readthedocs.io/ for the comprehensive documentation.

Support for My sCool Server
---------------------------
For support documentation related to the MSS project refer [Documentation and Support](http://mss-doc.readthedocs.io/en/latest/08-Useful%20Documentation%20and%20Support.html).

For issues specifically related to the My sCool Server report them at the [github issue tracker](https://github.com/cyberorg/myscoolserver/issues).

**NOTE:** Report issues or feature requests with applications and add-on contents on their respective bug trackers/forums, this space is for issues directly related to MSS only.

Also this place is not for support requests, use respective forums of applications for that purpose. 

We use Ubuntu-Mate as base, bugs for Ubuntu, Ubuntu Mate and packages from their respective repositories(or ppa) should be reported on their bug trackers.

Add-on content is not part of MSS, it is provided free of cost upon request from schools, use their respective forums for any issues with them or features needed.

Bugs in Ubuntu or applications
------------------------------
https://bugs.launchpad.net/

Fixes for those applications usually arrive via online update or in subsequent MSS releases.

Participate in Localisation of the MSS Documentation
---------------------------------------------------
Herein are a few guidelines to get one started quickly with the translation effort.

1. You should have the following packages installed in your environment -
 - Python 2.x+
 - [pip](https://pip.pypa.io/en/stable/installing/)
 - [sphinx](http://www.sphinx-doc.org/en/stable/tutorial.html#install-sphinx)
 - [sphinx-autobuild](https://pypi.python.org/pypi/sphinx-autobuild#installation)
 - [sphinx-intl](https://pypi.python.org/pypi/sphinx-intl#installation)

2. Ensure you have a `build/gettext` directory path under the docs directory. You may need to create it if you have done a fresh checkout.

3. After making any changes or adding to english documentation, extract document’s translatable messages into pot files:

	`make gettext`

4. Setup/Update your locale doc by running the following in the docs folder (for e.g. herein we are doing it for Gujarati - 'gu' locale):

    `sphinx-intl update -p build/gettext/ -l gu`

5. To test changes locally, run the following and open resulting html in web browser:

    `make -e SPHINXOPTS="-D language='gu'" html`

If the modifications do not fit in any of the .rst files under https://github.com/cyberorg/mss/tree/master/docs/source then create a new .rst file and add it in https://github.com/cyberorg/mss/blob/master/docs/source/index.rst under toctree. Execute steps 3 to 4 above thereafter.

To simply translate the existing manual to a specific locale fork the project, edit the .po files from the respective locale's directory `docs/source/locale/gu/LC_MESSAGES` and submit a pull request.

NOTE: DO NOT use "Edit on Github" at http://mss-doc-gu.readthedocs.io/gu/latest/ for translating the manual to a specific locale.

Checkout [RTD documentation](http://mss-doc.readthedocs.io/) and [Translating with sphinx-intl](http://www.sphinx-doc.org/en/stable/intl.html#translating-with-sphinx-intl) for a detailed guide to participate in this documentation project.
