Purpose
=======

`Cartographer`_ is a system that provides real-time simultaneous localization
and mapping (`SLAM`_) in 2D and 3D across multiple platforms and sensor
configurations.

trajectory extract: https://github.com/cartographer-project/cartographer_ros/issues/332 -> TrajectoryQuery

informations

```sh
# get trajectory_id
rosservice call /get_trajectory_states "{}" 
# get query submap
rosservice call /submap_query "trajectory_id: 0 submap_index: 0" 
# get trajectory points with timestamp
rosservice call /trajectory_query "trajectory_id: 0"
```

commands

```sh
# finishing
rosservice call /finish_trajectory "trajectory_id: 0"
# saving
rosservice call /write_state "filename: '${HOME}/Downloads/test_map.bag.pbstream' include_unfinished_submaps: false" 
# for localization in different place, better to write in launch file
/start_trajectorr
```

|video|

.. _Cartographer: https://github.com/googlecartographer/cartographer
.. _SLAM: https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping

Getting started
===============

* Learn to use Cartographer at `our Read the Docs site`_.
* You can ask a question by `creating an issue`_.

.. _our Read the Docs site: https://google-cartographer.readthedocs.io
.. _creating an issue: https://github.com/googlecartographer/cartographer_ros/issues/new?labels=question

Open house
==========

We regularly meet in an open-for-all Google hangout to discuss progress and plans for Cartographer.
You can join the `mailing list`_ to receive announcements.

The next Cartographer Open House Hangout is on **Thursday, May 9th 2019, 5pm CEST (8am PDT)** [`Hangouts link`_].

.. _mailing list: https://groups.google.com/forum/#!forum/google-cartographer
.. _Hangouts link: https://staging.talkgadget.google.com/hangouts/_/google.com/cartographeropenhouse

- March 14, 2019: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/190314/slides.pdf>`_
- February 21, 2019: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/190221/slides.pdf>`_
- January 17, 2019: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/190117/slides.pdf>`_
- November 22, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/181122/slides.pdf>`_
- October 25, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/181025/slides.pdf>`_
- September 13, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180913/slides.pdf>`_
- August 16, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180816/slides.pdf>`_
- August 2, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180802/slides.pdf>`_
- July 5, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180705/slides.pdf>`_
- June 21, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180621/slides.pdf>`_
- June 7, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180607/slides.pdf>`_
- May 24, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180524/slides.pdf>`_
- May 3, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180503/slides.pdf>`_
- March 29, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180329/slides.pdf>`_
- February 22, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180222/slides.pdf>`_
- February 8, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180208/slides.pdf>`_
- January 18, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180125/slides.pdf>`_
- January 11, 2018: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/180111/slides.pdf>`_
- December 7, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/171207/slides.pdf>`_
- November 23, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/171123/slides.pdf>`_
- November 9, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/171109/slides.pdf>`_
- October 26, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/171026/slides.pdf>`_
- October 12, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/171012/slides.pdf>`_
- September 14, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/170914/slides.pdf>`_
- August 17, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/170817/slides.pdf>`_
- July 20, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/170720/slides.pdf>`_
- July 6, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/170706/slides.pdf>`_
- June 22, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/170622/sildes.pdf>`_
- June 8, 2017: `Slides <https://storage.googleapis.com/cartographer-public-data/cartographer-open-house/170608/slides.pdf>`_

Contributing
============

You can find information about contributing to Cartographer at `our Contribution
page`_.

.. _our Contribution page: https://github.com/googlecartographer/cartographer/blob/master/CONTRIBUTING.md

.. |build| image:: https://travis-ci.org/googlecartographer/cartographer.svg?branch=master
    :alt: Build Status
    :scale: 100%
    :target: https://travis-ci.org/googlecartographer/cartographer
.. |docs| image:: https://readthedocs.org/projects/google-cartographer/badge/?version=latest
    :alt: Documentation Status
    :scale: 100%
    :target: https://google-cartographer.readthedocs.io/en/latest/?badge=latest
.. |license| image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
     :alt: Apache 2 license.
     :scale: 100%
     :target: https://github.com/googlecartographer/cartographer/blob/master/LICENSE
.. |video| image:: https://j.gifs.com/wp3BJM.gif
    :alt: Cartographer 3D SLAM Demo
    :scale: 100%
    :target: https://youtu.be/DM0dpHLhtX0
