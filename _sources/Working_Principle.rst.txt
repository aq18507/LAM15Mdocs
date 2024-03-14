Working principle
#################

The basic premise of the script is that the student will inputs variables that the script takes and calculates stresses and strains from. There are two possible ways of inputting data:

#. **MATLAB**
#. **Excel**

.. warning::
    Please note that the **Excel** functionality is not actively developed and for that reason, it must be used with caution. Any results should be compared with the equivalent **MATLAB** functionality.

Matlab
******

Edit three *input* scripts (``Details.mlx``, ``Material.mlx``, ``Laminate.mlx``). The student will then check the printed data (the function ``DataPrint.mlx``). After the data is checked, *calculation functions* are carried out for: the material properties (the function ``ABDCalc.mlx``); the thermal analysis (the function ``Thermal.mlx``); the load analysis (the function ``Loads.mlx``); and hygro analysis (the function ``Moisture.mlx``). The flow of the program is shown in Figure **X**.

The purpose of the script is to aid learning, therefore automation *is not* recommended. The 'slow' process of editing the three input scripts, running the program, checking the code and results is key to the design process. Using this tool as a black box is not the intended use-case. The calculation functions can be investigated by using the debugging function within Matlab~\cite{MATLAB_Debug}. This *is* recommended to cross-reference with hand calculations and compliment learning in lectures. Not fully understanding 'how' a code works is dangerous, particularly when written by well-intentioned but imperfect PhD students...

All equations used within the code can be found in the lecture notes. Some extra resources that were used for this script can be found in Reference [voyiadjis_mechanics_2005]_. 

Excel
*****

.. note::
    This function is not currently actively developed