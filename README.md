# How to install Drozer on macOS Catalina (By using pipenv)

[drozer](https://github.com/FSecureLABS/drozer) is the leading security testing framework for Android.
Frequently referenced in [OWASP MSTG](https://github.com/OWASP/owasp-mstg).

However, almost documents about installation are outdated, so I coudn't find how to install It on macOS Catalina.

I hope this document helps someone.

## Emvironment

- MacBook Pro (13-inch, 2018, Four Thunderbolt 3 Ports)
- macOS Catalina version:10.15.2（19C57）
- Python 2.7.16

## Build & Install

1. `git clone git@github.com:FSecureLABS/drozer.git`
1. `cd drozer`
1. `python2 --version`
    - python2 is required. check your installed version.
1. `pipenv --python 2.x.xx`
1. `pipenv shell`
1. edit setup.py with reference to [this comment](https://github.com/FSecureLABS/drozer/issues/357#issuecomment-546886215)
1. `python setup.py bdist_wheel`
    - bear up so much warnings
1. `pipenv install dist/drozer-2.4.3-py2-none-any.whl`

Maybe that's all.  
if you want to know Drozer command or testing techniques, see other great documents.
- [FSecureLABS/drozer](https://github.com/FSecureLABS/drozer)
- [Android Penetration Tools Walkthrough Series: Drozer](https://resources.infosecinstitute.com/android-penetration-tools-walkthrough-series-drozer/)
- [OWASP MSTG](https://github.com/OWASP/owasp-mstg)
