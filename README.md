# matplotlib_qtquick_playground

An updated version of the original.
Updated to qt 5.13.2, only the backend and QtQuick version 2 part.

Original README.md in README_org.md


Notes
=======

- backend and qml-files updated
- Not existing tostring_bgra function in line 118 of backend_qquick5agg.py
       stringBuffer = self.renderer._renderer.tostring_bgra()
  Ad hoc patch: add tostring_bgra to matplotlib/backends.backend_agg.py and use
        stringBuffer = self.renderer.tostring_bgra()

Console output:

The mouseover_set attribute was deprecated in Matplotlib 3.0 and will be removed in 3.2.

  artists = [a for a in event.inaxes.mouseover_set

  file:///home/sietse/.local/lib/python3.7/site-packages/PyQt5/Qt/qml/QtQuick/Controls.2/Universal/RangeSlider.qml: QML QQuickRangeSliderNode: Binding loop detected for property "value"

It basically works now, but when ending the program:

    QObject::startTimer: Timers can only be used with threads started with QThread
    QObject::startTimer: Timers can only be used with threads started with QThread
    Must construct a QGuiApplication first.
    Segmentation fault



Requirements
============

* Python >= 3.7
* PyQt = 5.13
* matplolib >= 3

License
=======

MIT License

Copyright (C) 2016 Frederic Collonval

The code for QtQuick Controls 2.0 makes used of the KDE Breeze Icons Theme (https://github.com/KDE/breeze-icons) distributed under LGPLv3

> The Breeze Icon Theme in icons/

> Copyright (C) 2014 Uri Herrera and others
