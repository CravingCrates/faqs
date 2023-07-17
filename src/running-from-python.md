# Running from Python

If you experience startup problems or crashes with the packaged builds of Anki
that you are unable to resolve, you can try running directly via Python as a
last resort.

The instructions below are provided for Windows users, as these problems seem
most prevalent on Windows, but a similar approach can be taken on other
platforms too.

1. Install <https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe>. Customize
   the install location, and choose `c:\python`
2. Open the Start menu, and open a Command Prompt.
3. Type in the following and hit enter:

```
\python\python -m venv \anki-venv
```

4. And then the following, which will take a while:

```
\anki-venv\scripts\pip install aqt orjson
```

5. Finally:

```
\anki-venv\scripts\anki
```

If that solves your problem, you can start Anki again in the future by repeating
steps 2 and 5.

If you still experience problems, you can try changing the Qt version:

```
\anki-venv\scripts\pip install pyqt5==5.15 pyqtwebengine==5.15.0
```

If that does not help either, and you have already followed all the steps on
[when problems occur](./when-problems-occur.md), then you may unfortunately be
out of luck.
