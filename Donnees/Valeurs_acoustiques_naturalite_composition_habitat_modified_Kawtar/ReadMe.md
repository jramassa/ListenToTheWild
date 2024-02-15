This is a ReadMe file for this Dataset.

# List of Folders:
- Naturalness_Index_seperated_by_site : For each of the 16 sites, the naturalness_index csv file was cut up in order to have, for each site, four csv files containing in each one of them the naturalness index for each of the four main classes which are : BE,BL,RE,RL (bleu estive, bleu lisiere, rouge estive et rouge lisiere). This is in order to have really small files to combine however we like in the future. For example, to make an only bleu estive dataset for example, or only a rouge sub-dataset, and so on. these files were used to create for example the Naturalness_Index_complete_by_site folder.

- Naturalness_Index_complete_by_site : For each of the 16 sites, the naturalness index information for all of the 4 main classes were gathered in one csv file, they are all ordered to be the exact following order : BE, BL, RE, RL. These csv files contain a new collumn that is called station_name, and corresponds to the station_name collumn in the corresponding valeur acoustique files. This will make it easier to merge the Valeurs_acoustiques and the naturalness datasets.

- Valeurs_acoustiques : Contains the acoustic indices that were calculated using recordings in each site. There is data from 2022 and 2023 and it is seperated into folders for each site.

- Valeurs_acoustiques_complete_by_site : The acoustique_indices csv file from the 2022 year were all merged for each site in order to create a new dataset containing the acoustic indices by site in the exact following order : BE, BL, RE, RL.

- Merged_Naturalness_Index_and_Valeurs_acoustiques_by_site : A dataset obtained by merging together the Naturalness_index data for each site with the Valeurs_acoustiques data found in the acoustic_indices.csv files for each site. This could allow a learning model to use the acoustic data from each recording and predict the naturalness mean and median. We could also use instead the seperated files (but in the correct order BE,BL,RE,RL) in order to put all the recordings data into one vector (matrice) for the model to learn from and then predict the naturalness mean and median for each one of the main four classes.

# The names of the different sites in case we need them for future reference:

    Antras_Isard:
    Ascou_Pailheres:
    Bestiac_Trimouns:
    Bethmale_Eychelle:
    Bonac_Orle:
    Couflens_Saubé:
    Goulier_Val_de_Sos:
    Merens_Comte:
    Mijanes_Estagnet:
    Mijanes_Trabesses:
    Montségur_Soularac:
    Orgeix_Coume:
    Orlu_RNCFS:
    Seix_Col_de_Pause:
    Sentein_Eylie:
    Ustou_Guzet-Neige:


# To build The Two following files for a given site:
- Nom_du_site_Bleu_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_bleu_du_site_a_changer naturalness_index_by_site.csv > Nom_du_site_Bleu_naturalness_index.csv
- Nom_du_site_Rouge_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_rouge_du_site_a_changer naturalness_index_by_site.csv > Nom_du_site_Rouge_naturalness_index.csv

==> These two files permit to take a look, for a given site, the mean, std and median of naturalness for a given color, blue or red. The estive/lisiere sites are combined.

# To build The Four following files for a given site:
==> Note: The following commands should be run in the repisotary of Valeurs_acoustiques__naturalite__composition_habitat

- Nom_du_site_Bleu_estive_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_bleu_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m estive > Nom_du_site_Bleu_estive_naturalness_index.csv

- Nom_du_site_Bleu_lisiere_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_bleu_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m lisiere > Nom_du_site_Bleu_lisiere_naturalness_index.csv

- Nom_du_site_Rouge_estive_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_rouge_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m estive > Nom_du_site_Rouge_estive_naturalness_index.csv

- Nom_du_site_Rouge_lisiere_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_rouge_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m lisiere > Nom_du_site_Rouge_lisiere_naturalness_index.csv

==> These four files allow us to have the same structure as the Valeurs acoustiques files for each Site. That way, for each site, we have the naturalness information in 4 groups of Bleu_estive, Bleu_lisiere, Rouge_estive et Rouge_lisiere

==>Here is an example:
csvgrep -c CODE_TRANS -m 529 naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m estive > Naturalness_Index_seperated_by_site/Ascou_Pailheres/Ascou_Pailheres_Bleu_estive_naturalness_index.csv


# To group two or more files from the Naturalness_Index_by_site in order to construct another data base
- Grouping two files, and giving them the groups : group1 and group2. We also decide to call the grouping column that we added new_collumn_name:
    csvstack -g group1,group2 -n new_collumn_name file1_name.csv file2_name.csv | csvcut -c CODE_TRANS,LAYER,mean_naturalness_100,new_collumn_name | csvlook

- We can save these files by using the > instead of csvlook:
    csvstack -g group1,group2 -n new_collumn_name file1_name.csv file2_name.csv | csvcut -c CODE_TRANS,LAYER,mean_naturalness_100,new_collumn_name > New_merged_dataset_name.csv

==> Here is an example for the Antras_Isard Site:
csvstack -g 2022/Antras_Isard/SM4610_702E_Bleu/Data/,2022/Antras_Isard/SM4564_702L_Bleu/Data/ -n station_name Antras_Isard_Bleu_estive_naturalness_index.csv Antras_Isard_Bleu_lisiere_naturalness_index.csv | csvcut -c CODE_TRANS,LAYER,mean_naturalness_100,station_name | csvlook

==>We can apply the example on four files,using the following codes for the four classes we already know : 
    2022/Antras_Isard/SM4610_702E_Bleu/Data/
    2022/Antras_Isard/SM4564_702L_Bleu/Data/
    2022/Antras_Isard/SM7134_235E_Rouge/Data/
    2022/Antras_Isard/SM7113_235L_Rouge/Data/

We find : 
csvstack -g 2022/Antras_Isard/SM4610_702E_Bleu/Data/,2022/Antras_Isard/SM4564_702L_Bleu/Data/,2022/Antras_Isard/SM7134_235E_Rouge/Data/,2022/Antras_Isard/SM7113_235L_Rouge/Data/ -n station_name Antras_Isard_Bleu_estive_naturalness_index.csv Antras_Isard_Bleu_lisiere_naturalness_index.csv Antras_Isard_Rouge_estive_naturalness_index.csv Antras_Isard_Rouge_lisiere_naturalness_index.csv | csvcut -c CODE_TRANS,LAYER,mean_naturalness_100,station_name | csvlook

# To group all the files related to one specific site in order to make a complete dataset with all the four classes in the following order : 
# BE,
# BL,
# RE,
# RL

- Note that what we mean by code_station_name is the value found in the station_name collumn in the Valeurs acoustiques/Site_name/class_name/acoustic_indices. For example, for Astras_Isard, the four code names found in the four files in Valeurs acoustiques folder are : 
-     2022/Antras_Isard/SM4610_702E_Bleu/Data/
-     2022/Antras_Isard/SM4564_702L_Bleu/Data/
-     2022/Antras_Isard/SM7134_235E_Rouge/Data/
-     2022/Antras_Isard/SM7113_235L_Rouge/Data/

- Here is the command to use : 
    csvstack -g code_station_name_be,code_station_name_bl,code_station_name_re,code_station_name_rl -n station_name file_1_be.csv file_2_bl.csv file_3_re.csv file_4_rl.csv > Nom_du_site_Complete_dataset_naturalness_index.csv

==>Example for the Anstras_Israd file
csvstack -g 2022/Antras_Isard/SM4610_702E_Bleu/Data/,2022/Antras_Isard/SM4564_702L_Bleu/Data/,2022/Antras_Isard/SM7134_235E_Rouge/Data/,2022/Antras_Isard/SM7113_235L_Rouge/Data/ -n station_name Antras_Isard_Bleu_estive_naturalness_index.csv Antras_Isard_Bleu_lisiere_naturalness_index.csv Antras_Isard_Rouge_estive_naturalness_index.csv Antras_Isard_Rouge_lisiere_naturalness_index.csv > Antras_Isard_Complete_dataset_naturalness_index.csv


# To group indices acoustiques files together for a specific site in order to have the same order as the ones in the Naturalness_index_by_site folder

==> Example for two files BE and BL for the Antras_Isard site:
    csvstack SM4610_702E_Bleu/acoustic_indices.csv SM4564_702L_Bleu/acoustic_indices.csv | ../../../test1.csv

==> Example of fusing the whole Antras_Isard folder : 
    csvstack SM4610_702E_Bleu/acoustic_indices.csv SM4564_702L_Bleu/acoustic_indices.csv SM7134_235E_Rouge/acoustic_indices.csv SM7113_235L_Rouge/acoustic_indices.csv > ../../../Valeurs_acoustiques_complete_by_site/Antras_Isard_valeurs_acoustiques_complete.csv


# To group indices acoustiques files with Naturalness_index_complete_by_site, since now we have the complete naturalness ones (with an additional collumn station_name that will help us join the two) and the complete acoustic values ones, in the exact same order

==> General command
csvjoin -c station_name test1.csv test2.csv > test3.csv

==> Example:
csvjoin -c station_name Valeurs_acoustiques_complete_by_site/Ustou_Guzet-Neige_valeurs_acoustiques_complete.csv Naturalness_Index_complete_by_site/Ustou_Guzet-Neige_complete_dataset_naturalness_index.csv > Merged_Naturalness_Index_and_Valeurs_acoustiques_by_site/Ustou_Guzet-Neige_merged_naturalness_valeurs_acoustiques.csv

