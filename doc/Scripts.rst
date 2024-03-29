Scripts
#######

This section describes each of the three input scripts, how they are designed and how to use them. The code primarily uses structures [MATLAB_Structures] to contain data. This keeps the workspace in ``Lam15m.mlx`` tidy and allows the user to (hopefully) intuitively look in the structures for information regarding the scripts information. (*I.e.* the data structure ``det``, contains information that was set in the ``Details.mlx`` script.) The three outputs from these scripts, ``det``, ``mat``, ``lam``, are typically the input into the calculation functions later in the script.

Details
*******

``Details.mlx`` is a script that contains the units and loading information for the laminate analysis program. The first section of code defines the units. The units are *only* used within the code for printing purposes. It is up to the code user to ensure the numbers they put in and the units they use are coherent and correct. The second section of the code defines the loading (mechanical, thermal and hygro). Each field within the data structure is an array that is explained within the code.

``Details.mlx`` does need to be edited by the user to define units and loading.

Material
********

``Material.mlx`` is a script that contains the material properties of eight different laminae. The lamina properties are taken from the CDM unit data sheet and are collected in Appendix~\ref{sec:app1}. The lamina materials each have a code that refers to: type of material (unidirectional or woven), type of modulus, type of fibre and type of matrix. All laminae initially coded in are epoxy. The unidirectional (UD) lamina properties are at 60% fibre volume fraction (:math:`V_f`). The woven (WV) lamina properties are at 50% :math:`V_f`. The units are initially coded to be in MPa, in line with using mm for other dimensions.

Strains to failure are in percentage strain (% :math:`\epsilon`), which, when considering a unit length of material, can be converted into actual strain (:math:`\epsilon`) by dividing by 100. :math:`\epsilon` can be converted into microstrain (:math:`\mu \epsilon`) by multiplying :math:`\epsilon` by :math:`1 \times 10^6`. By converting % :math:`\epsilon` to :math:`\epsilon`, the strengths to failure can also be calculated, should stress be needed. Additionally, coefficients of thermal expansion are included to calculate residual thermal stresses if a temperature difference is included. Residual thermal strains are 'used up' strain from the strains to failure, therefore any thermal loading will reduce the strains to failure of the lamina. A key is included that describes each material code.

``Material.mlx`` does not need to be edited by the user unless updated material properties are given.

Laminate
********

``Laminate.mlx`` is a script that defines the laminate to be analysed. The first section defines the stacking sequence, with the 'first' ply considered to be the 'bottom' of the laminate. The angles are given in degrees. Either manual input can be used (*i.e.* writing ``lam.angle = [45, -45, -45, 45];`` for a :math:`[\pm45]_s` laminate) or code that defines an array (*i.e.* ``lam.angle = ones(1,4)*90;`` for a :math:`[90_4]` laminate). Similarly, the laminate material choice is defined by the user. The laminate ply thickness is defined based on the material choice. A quick sanity check is carried out at the end of the script to ensure the arrays are the same length.

``Laminate.mlx`` does need to be edited by the user to define the laminate under investigation.