# GURPS Pylae

The original **GCA4 Data Set** included:

(**OK** if exists in *GCS MasterLib* / **Missing** for to be written)

* GURPS Basic Set 4th Ed **OK**
* files to remove Basic Set Skills and Equipment > TL 4 *not needed*
* GURPS Powers **OK**
* GURPS Supers **OK**
* GURPS Fantasy **OK**
* GURPS Low Tech **OK**
* GURPS Magic *(is this complete?)*
* GURPS Magic - Plant Spells **OK**
* GURPS Magic 4e - Clerical Magic *(does this exist?)*
* GURPS Martial Arts 4e.gdf **OK**
* GURPS Thaumatology 4e.gdf (**missing** Threshold Magic)
* GURPS Power-Ups 1 Imbuements 4e.gdf **OK**
* GURPS Power-Ups 2 Perks 4e.gdf **OK**
* GURPS Power-Ups 3 Talents.gdf **OK**
* GURPS Fantasy Equipment.gdf *(does this exist?)*
* Homebrew GURPS 4e Pylae.gdf **Missing**
* Pylae Template - Steppenläufer.gdf **Missing** -> all Pylae meta traits / races (problematic term!?) / animals!

# Initiative Attribute

$basic_speed + if(trait_level(Combat Reflexes) >= 1, 1, 0) + if(trait_level(Enhanced Time Sense) >= 1, 2, 0) - if(trait_level(Combat Paralysis) >= 1, 2, 0) + (if(skill_level(Tactics) >= 20, 2, 0) || if(skill_level(Tactics) >= 16, 1, 0) )
