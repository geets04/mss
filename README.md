#My sCool Server
Support for My sCool Server
---------------------------

Open Issue here https://github.com/cyberorg/myscoolserver/issues

NOTE: Report issues with applications on their respective bug trackers, this place is for issues directly related to MSS.

Also this place is not for support requests, use respective forums of applications for that purpose. We use Ubuntu-Mate, bugs for Ubuntu and Ubuntu Mate should be reported there:

Bugs in Ubuntu or applications
------------------------------
https://bugs.launchpad.net/

Support for Ubuntu
------------------
https://ubuntu-mate.org/community/  
https://answers.launchpad.net/  
https://ubuntu-mate.community/  
https://ubuntuforums.org/  

Fixes for those applications usually arrive via online update or in next releases.

MSS Documentation
-----------------
Checkout http://mss-doc.readthedocs.io/ for the documentation.

After making any changes in english, update gu by running the following in the docs folder:
    `sphinx-intl update -p build/gettext/ -l gu`

To test changes locally, run the following and open resulting html in web browser:
    `make -e SPHINXOPTS="-D language='gu'" html`

To translate the User manual in Gujarati edit the .po files from here: https://github.com/cyberorg/mss/tree/master/docs/source/locale/gu/LC_MESSAGES

NOTE: DO NOT use "Edit on Github" from http://mss-doc-gu.readthedocs.io/gu/latest/ for translating the manual in Gujarati

If the modifications do not fit in any of the .rst files under https://github.com/cyberorg/mss/tree/master/docs/source then create a new .rst file and add it in https://github.com/cyberorg/mss/blob/master/docs/source/index.rst under toctree.

