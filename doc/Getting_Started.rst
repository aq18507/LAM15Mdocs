Getting Started
###############

This page explains how to get started with LAM15M.

Minimum requirements
++++++++++++++++++++

* ``MATLAB``: A version of MATLAB must be installed that supports live scripts. It was written in version ``R2021b`` implying that it is likely compatible with future versions.
* ``Microsoft Excel``: Microsoft Excel or an equivalent program which allows ``.xlsx`` files to be edited must be installed the Excel import/export functionality within LAM15M is selected.
* ``Windows``: LAM15M is written to run on a PC running Windows 10.
* ``MacOS``: LAM15M is programmed such that it will also run on MacOS.

LAM15M was not tested on any ``Linux`` distro. That said, the only difference between the Mac and PC version is the assignment of the paths which are used to index the scripts which are different on a PC and Mac. This means it is likely that the inclusion of ``linux`` as an operating system will suffice using the same settings as for MacOS since they are both UNIX based operating systems.

OCTAVE is sometimes used instead of MATLAB. This was never tested on a version of OCTAVE, but input is greatly appreciated making this available to a wider audience.

Useful additional software
++++++++++++++++++++++++++

# ``GitHub``: Since this is still in active development it is useful to utilise **GitHub** to pull the current and most up-to-date version as new modules might be added, performance increased and errors eliminated.

How to install Lam15M
+++++++++++++++++++++

* Used the download button in GitHub to get this repository located in the top right hand corner.
* Use the Git on to fetch this repository. Note that there is a difference in how this works between Windows and MacOS.

Windows
-------

.. warning::
    Git is not installed by default on Windows. To check run ``git -v`` in the command prompt. If it returns a version then it is installed. If not, install GitHub `Git Download and install guide <https://github.com/git-guides/install-git>`_.

#. Go to the directory in which the config files should reside.
#. Clone this git repository into an easily accessible location (ideally somewhere on the ``C`` drive on Windows).
#. Right-click and select ``Open Git Bash here``.
#. Use the ``git clone https://github.com/aq18507/LAM15M.git`` command and hit enter. Now the directory is cloned.

Mac
-----

.. note::
    Git is installed by default on MacOS. To check the version run ``git -v`` in the terminal.

#. Open the terminal program.
#. Use the change directory ``cd /[your directory]/`` command to move to the directory of your choice.
#. Use the ``git clone https://github.com/aq18507/LAM15M.git`` command and hit enter. Now the directory is cloned.