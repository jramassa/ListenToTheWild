# To build The Two following files for a given site:
- Nom_du_site_Bleu_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_bleu_du_site_a_changer naturalness_index_by_site.csv > Nom_du_site_Bleu_naturalness_index.csv
- Nom_du_site_Rouge_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_rouge_du_site_a_changer naturalness_index_by_site.csv > Nom_du_site_Rouge_naturalness_index.csv

==> These two files permit to take a look, for a given site, the mean, std and median of naturalness for a given color, blue or red. The estive/lisiere sites are combined.

# To build The Four following files for a given site:
- Nom_du_site_Rouge_estive_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_rouge_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m estive > Nom_du_site_Rouge_estive_naturalness_index.csv

- Nom_du_site_Rouge_lisiere_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_rouge_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m lisiere > Nom_du_site_Rouge_lisiere_naturalness_index.csv

- Nom_du_site_Bleu_estive_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_bleu_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m estive > Nom_du_site_Bleu_estive_naturalness_index.csv

- Nom_du_site_Bleu_lisiere_naturalness_index.csv : 
    csvgrep -c CODE_TRANS -m code_couleur_bleu_du_site_a_changer naturalness_index_by_site.csv | csvgrep -c CODE_TRANS -m lisiere > Nom_du_site_Bleu_lisiere_naturalness_index.csv

==> These four files allow us to have the same structure as the Valeurs acoustiques files for each Site. That way, for each site, we have the naturalness information in 4 groups of Bleu_estive, Bleu_lisiere, Rouge_estive et Rouge_lisiere


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

# To group all the files related to one specific site in order to make a complete dataset with all the four classes in the following order : BE,BL,RE,RL

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



