# beh-analysis-hotosm-tm
```mermaid
C4Component
    title Component diagram for Process Analysis in Humanitarian VGI

    System_Ext(hot, "HOT-TM API")
    System_Ext(bla, "Bunting Labs API")

    Boundary(syb, "beh-analysis-hotosm-tm", ""){
        Component(dow, "download_data.ipynb")
        Component(bud, "building_density.ipynb")
        Component(dpp, "Data_preprocessing.ipynb")
        Component(pan, "Process_Analysis.Rmd")
    }

    Component_Ext(fil, "Intermediate files")
 
    BiRel(hot, dow, "API calls", "JSON/HTTPS")
    UpdateRelStyle(hot, dow, $offsetX="-80", $offsetY="20")

    BiRel(bla, dow, "API calls", "JSON/HTTPS")
    UpdateRelStyle(bla, dow, $offsetX="-110", $offsetY="20")

    BiRel(fil, dow, "")
    BiRel(fil, bud, "")
    BiRel(fil, dpp, "")
    BiRel(fil, pan, "")
```


This project has received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No 955569.
The opinions expressed in this document reflect only the author’s view and in no way reflect the European Commission’s opinions. The European Commission is not responsible for any use that may be made of the information it contains.
