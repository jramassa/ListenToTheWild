This file contains all the commands used to join the four classes naturalness_indexes for each site. It is a bit long and tedious hence the reason why they were written in this file in case they may need to be used again.

# List of station_name by site, in order to make it easy to join the naturalness_index_by_site four classes into one file:

    Antras_Isard:
2022/Antras_Isard/SM4610_702E_Bleu/Data/
2022/Antras_Isard/SM4564_702L_Bleu/Data/
2022/Antras_Isard/SM7134_235E_Rouge/Data/
2022/Antras_Isard/SM7113_235L_Rouge/Data/

csvstack -g 2022/Antras_Isard/SM4610_702E_Bleu/Data/,2022/Antras_Isard/SM4564_702L_Bleu/Data/,2022/Antras_Isard/SM7134_235E_Rouge/Data/,2022/Antras_Isard/SM7113_235L_Rouge/Data/ -n station_name Antras_Isard/Antras_Isard_Bleu_estive_naturalness_index.csv Antras_Isard/Antras_Isard_Bleu_lisiere_naturalness_index.csv Antras_Isard/Antras_Isard_Rouge_estive_naturalness_index.csv Antras_Isard/Antras_Isard_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Antras_Isard_complete_dataset_naturalness_index.csv

    Ascou_Pailheres:
2022/Ascou_Pailheres/SM5744_529E_Bleu/Data/
2022/Ascou_Pailheres/SM5810_529L_Bleu/Data/
2022/Ascou_Pailheres/SM6988_372E_Rouge/Data/
2022/Ascou_Pailheres/SM7137_372L_Rouge/Data/

csvstack -g 2022/Ascou_Pailheres/SM5744_529E_Bleu/Data/,2022/Ascou_Pailheres/SM5810_529L_Bleu/Data/,2022/Ascou_Pailheres/SM6988_372E_Rouge/Data/,2022/Ascou_Pailheres/SM7137_372L_Rouge/Data/ -n station_name Ascou_Pailheres/Ascou_Pailheres_Bleu_estive_naturalness_index.csv Ascou_Pailheres/Ascou_Pailheres_Bleu_lisiere_naturalness_index.csv Ascou_Pailheres/Ascou_Pailheres_Rouge_estive_naturalness_index.csv Ascou_Pailheres/Ascou_Pailheres_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Ascou_Pailheres_complete_dataset_naturalness_index.csv

    Bestiac_Trimouns:
2022/Bestiac_Trimouns/SM6988_638E_Bleu/Data/
2022/Bestiac_Trimouns/SM7108_638L_Bleu/Data/
2022/Bestiac_Trimouns/SM7140_641E_Rouge/Data/
2022/Bestiac_Trimouns/SM7113_641L_Rouge/Data/

csvstack -g 2022/Bestiac_Trimouns/SM6988_638E_Bleu/Data/,2022/Bestiac_Trimouns/SM7108_638L_Bleu/Data/,2022/Bestiac_Trimouns/SM7140_641E_Rouge/Data/,2022/Bestiac_Trimouns/SM7113_641L_Rouge/Data/ -n station_name Bestiac_Trimouns/Bestiac_Trimouns_Bleu_estive_naturalness_index.csv Bestiac_Trimouns/Bestiac_Trimouns_Bleu_lisiere_naturalness_index.csv Bestiac_Trimouns/Bestiac_Trimouns_Rouge_estive_naturalness_index.csv Bestiac_Trimouns/Bestiac_Trimouns_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Bestiac_Trimouns_complete_dataset_naturalness_index.csv

    Bethmale_Eychelle:
2022/Bethmale_Eychelle/SM4564_415E_Bleu/Data/
2022/Bethmale_Eychelle/SM6936_415L_Bleu/Data/
2022/Bethmale_Eychelle/SM7113_256E_Rouge/Data/
2022/Bethmale_Eychelle/SM7140_256L_Rouge/Data/

csvstack -g 2022/Bethmale_Eychelle/SM4564_415E_Bleu/Data/,2022/Bethmale_Eychelle/SM6936_415L_Bleu/Data/,2022/Bethmale_Eychelle/SM7113_256E_Rouge/Data/,2022/Bethmale_Eychelle/SM7140_256L_Rouge/Data/ -n station_name Bethmale_Eychelle/Bethmale_Eychelle_Bleu_estive_naturalness_index.csv Bethmale_Eychelle/Bethmale_Eychelle_Bleu_lisiere_naturalness_index.csv Bethmale_Eychelle/Bethmale_Eychelle_Rouge_estive_naturalness_index.csv Bethmale_Eychelle/Bethmale_Eychelle_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Bethmale_Eychelle_complete_dataset_naturalness_index.csv

    Bonac_Orle:
2022/Bonac_Orle/SM4610_401E_Bleu/Data/
2022/Bonac_Orle/SM6965_401L_Bleu/Data/
2022/Bonac_Orle/SM7134_402E_Rouge/Data/
2022/Bonac_Orle/SM4559_402L_Rouge/Data/

csvstack -g 2022/Bonac_Orle/SM4610_401E_Bleu/Data/,2022/Bonac_Orle/SM6965_401L_Bleu/Data/,2022/Bonac_Orle/SM7134_402E_Rouge/Data/,2022/Bonac_Orle/SM4559_402L_Rouge/Data/ -n station_name Bonac_Orle/Bonac_Orle_Bleu_estive_naturalness_index.csv Bonac_Orle/Bonac_Orle_Bleu_lisiere_naturalness_index.csv Bonac_Orle/Bonac_Orle_Rouge_estive_naturalness_index.csv Bonac_Orle/Bonac_Orle_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Bonac_Orle_complete_dataset_naturalness_index.csv

    Couflens_Saubé:
2022/Couflens_Saubé/SM6989_564E_Bleu/Data/
2022/Couflens_Saubé/SM7208_564L_Bleu/Data/

csvstack -g 2022/Couflens_Saubé/SM6989_564E_Bleu/Data/,2022/Couflens_Saubé/SM7208_564L_Bleu/Data/ -n station_name Couflens_Saubé/Couflens_Saubé_Bleu_estive_naturalness_index.csv Couflens_Saubé/Couflens_Saubé_Bleu_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Couflens_Saubé_complete_dataset_naturalness_index.csv

    Goulier_Val_de_Sos:
2022/Goulier_Val_de_Sos/SM6965_474E_Bleu/Data/
2022/Goulier_Val_de_Sos/SM4559_474L_Bleu/Data/
2022/Goulier_Val_de_Sos/SM6936_473E_Rouge/Data/
2022/Goulier_Val_de_Sos/SM7140_473L_Rouge/Data/

csvstack -g 2022/Goulier_Val_de_Sos/SM6965_474E_Bleu/Data/,2022/Goulier_Val_de_Sos/SM4559_474L_Bleu/Data/,2022/Goulier_Val_de_Sos/SM6936_473E_Rouge/Data/,2022/Goulier_Val_de_Sos/SM7140_473L_Rouge/Data/ -n station_name Goulier_Val_de_Sos/Goulier_Val_de_Sos_Bleu_estive_naturalness_index.csv Goulier_Val_de_Sos/Goulier_Val_de_Sos_Bleu_lisiere_naturalness_index.csv Goulier_Val_de_Sos/Goulier_Val_de_Sos_Rouge_estive_naturalness_index.csv Goulier_Val_de_Sos/Goulier_Val_de_Sos_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Goulier_Val_de_Sos_complete_dataset_naturalness_index.csv

    Merens_Comte:
2022/Merens_Comte/SM5744_349E_Bleu/Data/
2022/Merens_Comte/SM5810_349L_Bleu/Data/
2022/Merens_Comte/SM6988_509E_Rouge/Data/

csvstack -g 2022/Merens_Comte/SM5744_349E_Bleu/Data/,2022/Merens_Comte/SM5810_349L_Bleu/Data/,2022/Merens_Comte/SM6988_509E_Rouge/Data/ -n station_name Merens_Comte/Merens_Comte_Bleu_estive_naturalness_index.csv Merens_Comte/Merens_Comte_Bleu_lisiere_naturalness_index.csv Merens_Comte/Merens_Comte_Rouge_estive_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Merens_Comte_complete_dataset_naturalness_index.csv

    Mijanes_Estagnet:
2022/Mijanes_Estagnet/SM7142_374E_Bleu/Data/
2022/Mijanes_Estagnet/SM7175_374L_Bleu/Data/
2022/Mijanes_Estagnet/SM5765_375E_Rouge/Data/
2022/Mijanes_Estagnet/SM7108_375L_Rouge/Data/

csvstack -g 2022/Mijanes_Estagnet/SM7142_374E_Bleu/Data/,2022/Mijanes_Estagnet/SM7175_374L_Bleu/Data/,2022/Mijanes_Estagnet/SM5765_375E_Rouge/Data/,2022/Mijanes_Estagnet/SM7108_375L_Rouge/Data/ -n station_name Mijanes_Estagnet/Mijanes_Estagnet_Bleu_estive_naturalness_index.csv Mijanes_Estagnet/Mijanes_Estagnet_Bleu_lisiere_naturalness_index.csv Mijanes_Estagnet/Mijanes_Estagnet_Rouge_estive_naturalness_index.csv Mijanes_Estagnet/Mijanes_Estagnet_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Mijanes_Estagnet_complete_dataset_naturalness_index.csv

    Mijanes_Trabesses:
2022/Mijanes_Trabesses/SM5744_530E_Bleu/Data/
2022/Mijanes_Trabesses/SM7137_530L_Bleu/Data/
2022/Mijanes_Trabesses/SM5810_373E_Rouge/Data/
2022/Mijanes_Trabesses/SM6988_373L_Rouge/Data/

csvstack -g 2022/Mijanes_Trabesses/SM5744_530E_Bleu/Data/,2022/Mijanes_Trabesses/SM7137_530L_Bleu/Data/,2022/Mijanes_Trabesses/SM5810_373E_Rouge/Data/,2022/Mijanes_Trabesses/SM6988_373L_Rouge/Data/ -n station_name Mijanes_Trabesses/Mijanes_Trabesses_Bleu_estive_naturalness_index.csv Mijanes_Trabesses/Mijanes_Trabesses_Bleu_lisiere_naturalness_index.csv Mijanes_Trabesses/Mijanes_Trabesses_Rouge_estive_naturalness_index.csv Mijanes_Trabesses/Mijanes_Trabesses_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Mijanes_Trabesses_complete_dataset_naturalness_index.csv

    Montségur_Soularac:
2022/Montségur_Soularac/SM6992_626E_Bleu/Data/
2022/Montségur_Soularac/SM5802_626L_Bleu/Data/
2022/Montségur_Soularac/SM5760_628E_Rouge/Data/
2022/Montségur_Soularac/SM7107_628L_Rouge/Data/

csvstack -g 2022/Montségur_Soularac/SM6992_626E_Bleu/Data/,2022/Montségur_Soularac/SM5802_626L_Bleu/Data/,2022/Montségur_Soularac/SM5760_628E_Rouge/Data/,2022/Montségur_Soularac/SM7107_628L_Rouge/Data/ -n station_name Montségur_Soularac/Montségur_Soularac_Bleu_estive_naturalness_index.csv Montségur_Soularac/Montségur_Soularac_Bleu_lisiere_naturalness_index.csv Montségur_Soularac/Montségur_Soularac_Rouge_estive_naturalness_index.csv Montségur_Soularac/Montségur_Soularac_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Montségur_Soularac_complete_dataset_naturalness_index.csv

    Orgeix_Coume:
2022/Orgeix_Coume/SM7142_369E_Bleu/Data/
2022/Orgeix_Coume/SM7175_369L_Bleu/Data/
2022/Orgeix_Coume/SM7108_517E_Rouge/Data/
2022/Orgeix_Coume/SM5765_517L_Rouge/Data/

csvstack -g 2022/Orgeix_Coume/SM7142_369E_Bleu/Data/,2022/Orgeix_Coume/SM7175_369L_Bleu/Data/,2022/Orgeix_Coume/SM7108_517E_Rouge/Data/,2022/Orgeix_Coume/SM5765_517L_Rouge/Data/ -n station_name Orgeix_Coume/Orgeix_Coume_Bleu_estive_naturalness_index.csv Orgeix_Coume/Orgeix_Coume_Bleu_lisiere_naturalness_index.csv Orgeix_Coume/Orgeix_Coume_Rouge_estive_naturalness_index.csv Orgeix_Coume/Orgeix_Coume_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Orgeix_Coume_complete_dataset_naturalness_index.csv

    Orlu_RNCFS:
2022/Orlu_RNCFS/SM5810_682E_Bleu/Data/
2022/Orlu_RNCFS/SM7175_682L_Bleu/Data/
2022/Orlu_RNCFS/SM6936_522E_Rouge/Data/
2022/Orlu_RNCFS/SM7142_522L_Rouge/Data/

csvstack -g 2022/Orlu_RNCFS/SM5810_682E_Bleu/Data/,2022/Orlu_RNCFS/SM7175_682L_Bleu/Data/,2022/Orlu_RNCFS/SM6936_522E_Rouge/Data/,2022/Orlu_RNCFS/SM7142_522L_Rouge/Data/ -n station_name Orlu_RNCFS/Orlu_RNCFS_Bleu_estive_naturalness_index.csv Orlu_RNCFS/Orlu_RNCFS_Bleu_lisiere_naturalness_index.csv Orlu_RNCFS/Orlu_RNCFS_Rouge_estive_naturalness_index.csv Orlu_RNCFS/Orlu_RNCFS_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Orlu_RNCFS_complete_dataset_naturalness_index.csv

    Seix_Col_de_Pause:
2022/Seix_Col_de_Pause/SM4610_424E_Bleu/Data/
2022/Seix_Col_de_Pause/SM4559_424L_Bleu/Data/
2022/Seix_Col_de_Pause/SM7134_413E_Rouge/Data/
2022/Seix_Col_de_Pause/SM6965_413L_Rouge/Data/

csvstack -g 2022/Seix_Col_de_Pause/SM4610_424E_Bleu/Data/,2022/Seix_Col_de_Pause/SM4559_424L_Bleu/Data/,2022/Seix_Col_de_Pause/SM7134_413E_Rouge/Data/,2022/Seix_Col_de_Pause/SM6965_413L_Rouge/Data/ -n station_name Seix_Col_de_Pause/Seix_Col_de_Pause_Bleu_estive_naturalness_index.csv Seix_Col_de_Pause/Seix_Col_de_Pause_Bleu_lisiere_naturalness_index.csv Seix_Col_de_Pause/Seix_Col_de_Pause_Rouge_estive_naturalness_index.csv Seix_Col_de_Pause/Seix_Col_de_Pause_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Seix_Col_de_Pause_complete_dataset_naturalness_index.csv

    Sentein_Eylie:
2022/Sentein_Eylie/SM6989_245E_Bleu/Data/
2022/Sentein_Eylie/SM7208_245L_Bleu/Data/
2022/Sentein_Eylie/SM7112_244E_Rouge/Data/
2022/Sentein_Eylie/SM7138_244L_Rouge/Data/

csvstack -g 2022/Sentein_Eylie/SM6989_245E_Bleu/Data/,2022/Sentein_Eylie/SM7208_245L_Bleu/Data/,2022/Sentein_Eylie/SM7112_244E_Rouge/Data/,2022/Sentein_Eylie/SM7138_244L_Rouge/Data/ -n station_name Sentein_Eylie/Sentein_Eylie_Bleu_estive_naturalness_index.csv Sentein_Eylie/Sentein_Eylie_Bleu_lisiere_naturalness_index.csv Sentein_Eylie/Sentein_Eylie_Rouge_estive_naturalness_index.csv Sentein_Eylie/Sentein_Eylie_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Sentein_Eylie_complete_dataset_naturalness_index.csv

    Ustou_Guzet-Neige:
2022/Ustou_Guzet-Neige/SM7175_573E_Rouge/Data/
2022/Ustou_Guzet-Neige/SM7108_573L_Rouge/Data/

csvstack -g 2022/Ustou_Guzet-Neige/SM7175_573E_Rouge/Data/,2022/Ustou_Guzet-Neige/SM7108_573L_Rouge/Data/ -n station_name Ustou_Guzet-Neige/Ustou_Guzet-Neige_Rouge_estive_naturalness_index.csv Ustou_Guzet-Neige/Ustou_Guzet-Neige_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Ustou_Guzet-Neige_complete_dataset_naturalness_index.csv


    Command writing help
csvstack -g 
2022/Antras_Isard/SM4610_702E_Bleu/Data/,
2022/Antras_Isard/SM4564_702L_Bleu/Data/,
2022/Antras_Isard/SM7134_235E_Rouge/Data/,
2022/Antras_Isard/SM7113_235L_Rouge/Data/ 
-n station_name 
Nom_du_site/Nom_du_site_Bleu_estive_naturalness_index.csv Nom_du_site/Nom_du_site_Bleu_lisiere_naturalness_index.csv Nom_du_site/Nom_du_site_Rouge_estive_naturalness_index.csv Nom_du_site/Nom_du_site_Rouge_lisiere_naturalness_index.csv > ../Naturalness_Index_complete_by_site/Nom_du_site_complete_dataset_naturalness_index.csv


