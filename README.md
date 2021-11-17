# urban_clm5
Version 2.1


March 15, 2019, 9:02 AM

1, do something with green roof��s structure in initVerticalMod.F90 and get rid of hasBedrock for greenroof

2, UrbanParamsType. F90: add new namelist inputs: green roof albedo and green roof soil depth

3, SoilTemperture.F90: Change CV, thermal conductivity for green roof

still need to deal the boundary condition for green roofs

4, add new options like green_roof_albedo and green_roof_soil_depth

===============================
Version 2.1.1


March 18, 2019 12:09 PM

1, irrigation related 

SoilHydrologyMod.F90, WaterStateType.F90, BalanceCheckMod.F90

2, fixed a bug in TemperatureType.F90 about adding t_roof_surface, t_greenroof_surface, t_whiteroof_surface in restarts (this has not entered CASE7 but should not affect the code)


April 23, 2019

1, fix a problem in BalanceCheckMod.F90 that prevented using green roofs without irrigation. Now one can have green roofs without irrigation. 

===============================
Version 2.1.2


May 26, 2019

1, add temperature scaling for studying white roof


===============================
Version 2.1.3


July 23, 2019

1, add urban surface flux output for studying white roof


===============================
Version 2.1.4


August 19, 2019

1, modify temperature scaling for studying white roof 

2, add output to compute relative efficiency of urban surface energy flux


===============================
Version 2.1.5


August 23, 2019

1, add stomatal resistance for green roof evapotranspiration 

2, add new options like green_roof_rsmin and green_roof_watwilt 


September 26, 2019

1, fixed a bug in SoilHydrologyMod.F90 about green roof irrigation initialization. Now one can get green roof water added per unit area on green roofs.

2, add output for studying green roof


===============================
Version 2.2


October 30, 2019

1, modify initInterp for warm spinup, initInterpMindist.F90

2, modify the maximum green roof soil moisture after irrigation, SoilHydrologyMod.F90

December 10, 2019

1, fix a problem in subgridRestMod.F90 that prevented using correct green roof column weights. Now one can restart green roof case from zero green roof weights cases.


===============================
Version 2.2.1


June 20, 2020

1, add new options for global uniform green roof properties like green_roof_pct_clay, green_roof_pct_sand, green_roof_fmax, green_roof_slope

2, deal with the boundary condition for green roofs using BUILDING_TEMP_METHOD_SIMPLE, (building_temp_method = 0, simpler method (clm4_5))), SoilTemperatureMod.F90, SoilFluxesMod.F90

3, modify the calculation of green roof vertical soil properties based on soil texture from 10 layer input dataset, SoilStateInitTimeConstMod.F90

4, modify the green roof stomatal resistance parameterization, UrbanFluxesMod.F90


===============================
Version 2.3


July 18, 2020

1, deal with the boundary condition for green roofs using BUILDING_TEMP_METHOD_PROG, (building_temp_method = 1, prognostic calculation of interior building temp (clm5_0)), UrbBuildTempOleson2015Mod.F90, SoilTemperatureMod.F90


===============================
Version 2.3.1


December 14, 2020

1, add new options for green roof properties like green_roof_watwilt, green_roof_watfc, green_roof_watsat, green_roof_bsw, green_roof_sucsat, green_roof_xksat 

2, modify cv_greenroof and thk_greenroof according to THU site, SoilTemperatureMod.F90

3, modify the green roof stomatal resistance parameterization, UrbanFluxesMod.F90  


January 26, 2021

1, modify the green roof irrigation scheme to avoid irrigation when soil includes ice, SoilHydrologyMod.F90

2, modify the roof surface temperatures and fluxes output

===============================
Version 2.3.2


June 10, 2021

1, add output for a forcing-feedback framework in terms of sensitivity of Ta to anthropogenic heat in urban areas


===============================
Version 2.3.3

November 17, 2021

1, add output for analysing the contrasting responses of urban and rural surface climates to heat waves
