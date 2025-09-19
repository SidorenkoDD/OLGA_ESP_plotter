# OLGA Head & Rate Plotter module
## Description
This module, in conjunction with the OLGA model, allows to build the pressure and flow characteristics of the ESP.
## How to use
1. Set ESP in OLGA model and choose GASDEGRADATION mode.
        
        Use [pyfas](https://github.com/gpagliuca/pyfas) module to create your head & rate characteristics

2. Use ParametricStudy to calculate cases.
3. After calculation create OLGAHRPlotter object and set path to ParametricStudy results folder.
    
    This object automatically finds all .tpl-files in folder and parses them on initialization.
4. Use OLGAHRPlotter.plot()

    Example: 

        esp_plotter_obj = OLGAHRPlotter(folder_path)
        esp_plotter_obj.plot() - dP & rate plot
        esp_plotter_obj.plot(variable = 'Head') - head & rate plot


