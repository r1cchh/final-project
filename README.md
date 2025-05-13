# Noslēguma projekts - Automatizēta failu sakārtošana

## Apraksts
Izmantojot internetu bieži sanāk lejupielādēt daudz un dažādus failus. Laika gaitā lejupielādētie faili sakrājas vienā lejupielāžu mapē. Šis noved pie problēmas, ka šī mape ir diezgan nepārskatāma, jo faili ir sakārtoti tikai pēc to vecuma un šīs problēmas rezultātā var gadīties pazaudēt svarīgu dokumentu, gadījumā ja ir aizmirsies dokumenta nosaukums. Šī projekta uzdevums bija izveidot sistēmu, kas automātiski sakārto failus pēc to tipa, pārvietojot tos uz atbilstošām apakšmapēm. Šādā veidā lietotāja izvēlētā mape kļūst organizētāka un vieglāk pārskatāmāka. Šo sistēmu var izmantot lai sakārtotu jebkuru mapi, jo galu galā lejupielāžu mape arī ir mape.

## Izmantotās bibliotēkas
**os** bibliotēka ļauj piekļūt operētājsistēmas failu struktūrai. Ar tās palīdzību tiek iegūti visi mapē esošie faili, kā arī iespēja izveidot jaunas mapes.

**shutil** tiek izmantota, lai pārvietotu failus. Ar tās palīdzību faili tiek fiziski pārvietoti uz atbilstošajām kategoriju mapēm.

**datetime** bibliotēka ļauj reģistrēt katra pārvietotā faila laika zīmogu. To izmanto, lai vēlāk Excel tabulā un teksta failā varētu redzēt, kad tieši katrs fails ticis pārvietots.

**openpyxl** bibliotēka tiek izmantota darbam ar Excel failiem. Šajā projektā tā ļauj izveidot, atvērt un rediģēt Excel dokumentu, kurā tiek pierakstīta visa informācija par pārvietotajiem failiem.

## Datu struktūra
Projektā tika arī izveidota datu struktūra ar klasi FileRecord. Šis ir strukturēts veids, lai glabātu un apstrādātu informāciju par katru pārvietoto failu. Šī datu struktūra satur datus kā faila nosaukums, paplašinājums, kategorija, galamērķa mape un laika zīmogs, kad pārvietošana notika. Šī struktūra ļauj vienkāršāk un pārskatāmāk organizēt datus. Tā vietā, lai informācija tiktu glabāta vairākos nesaistītos sarakstos vai vārdnīcās, FileRecord palīdz ar datu grupēšanu vienā objektā.

## Programmas izmantošana
1.	Lejupielādē projektu no GitHub vai nokopē .py failu uz savu datoru.

2.	Atver failu redaktorā (piemēram, VS Code) un pārliecinies, ka datorā ir instalētas nepieciešamās Python bibliotēkas:

    •	openpyxl (var uzstādīt ar komandu pip install openpyxl)

3.	Maini mērķa mapes ceļu. Noklusētā vērtība ir ceļš uz lejupielāžu mapi (mainīgais DOWNLOADS_FOLDER). To var aizvietot ar jebkuru citu mapes ceļu, kuru vēlies sakārtot:

    •	DOWNLOADS_FOLDER = r"C:\Users\lietotājvārds\Lejupielādes"

4.	Palaiž programmu. Programma automātiski:

    •	Sakārtos visus failus apakšmapēs pēc to tipa (piemēram, Documents, Images, Videos utt.).

    •	Pierakstīs katra pārvietotā faila informāciju teksta un Excel failos (organizer_log.txt un organizer_log.xlsx).
