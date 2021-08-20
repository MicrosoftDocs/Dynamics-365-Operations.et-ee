---
title: Elektrooniline aruandlus. Nõutavate konfiguratsioonide loomine andmete importimiseks välisest failist
description: Selles teemas kirjeldatakse, kuidas kujundada elektroonilise aruandluse konfiguratsioone andmete importimiseks välisest failist rakendusse Microsoft Dynamics 365 Finance.
author: NickSelin
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eaa35baae8e030d8a8b7ce903554c4876c874b48cfd72d6ac278cf4c0e8a6e8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720852"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>Elektrooniline aruandlus. Nõutavate konfiguratsioonide loomine andmete importimiseks välisest failist

[!include [banner](../../includes/banner.md)]

Järgmised juhised selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab kujundada elektroonilise aruandluse (ER) konfiguratsioone, et importida andmeid välisest failist rakendusse. Juhendit järgides loote näidisettevõtte Litware, Inc. jaoks vajalikud ER-i konfiguratsioonid. Juhendis ülesannete lõpetamiseks peab esmalt täitma juhises „ER Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud toimingud. Need toimingud saab lõpule viia USMF-i andmekomplekti abil. Samuti peate alla laadima ja kohalikult talletama järgmised failid. 

| Sisu kirjeldus                       | Faili nimi                                     |
|-------------------------------------------|-----------------------------------------------|
| ER-i andmemudeli konfiguratsioon- 1099 | [1099mudel,xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| ER vormingu konfiguratsioon - 1099    | [1099vorming.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| CSV-vormingus sissetuleva dokumendi näidis                          | [1099sissekanded.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| Sissetuleva dokumendi andmete haldamise töövihiku näidis                          | [1099sissekanded.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

Elektrooniline aruandlus pakub ärikasutajatele võimalust konfigureerida väliste XML- või TXT-vormingus andmefailide importimisprotsessi. Esmalt tuleb imporditavate andmete tähistamiseks kujundada abstraktse andmemudeli ja elektroonilise aruandluse andmemudeli konfiguratsioon. Järgmisena peate määratlema imporditava faili struktuuri ja meetodi, mida kasutate andmete portimiseks failist abstraktseks andmemudeliks. Abstraktse andmemudeli jaoks tuleb luua elektroonilise aruandluse vormingu konfiguratsioon, mis vastendab kujundatud andmemudelile. Seejärel tuleb andmemudeli konfiguratsiooni laiendada vastendamisega, mis kirjeldab, kuidas imporditud andmed püsivad abstraktse andmemudelina ja kuidas seda kasutatakse tabelite värskendamiseks.  Elektroonilise aruandluse andmemudeli konfiguratsiooni tuleb täiendada uue mudeli vastendusega, mis kirjeldab andmemudeli sidumist rakenduse sihtkohtadega.  

Järgmine stsenaarium näitab elektroonilise aruandluse andmete importimise võimalusi. See hõlmab hankijakandeid, mida jälgitakse väliselt ja seejärel imporditakse, et nende kohta hiljem 1099 hankija tasakaalustuses aruandlust teha.   

## <a name="add-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.

    Veenduge, et konfiguratsioonipakkuja näidisettevõttele „Litware, Inc.” on saadaval ja märgitud aktiivseks. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks” esitatud juhised.   

2. Klõpsake valikut Aruandluse konfiguratsioonid.

    Andmeimpordi toetamiseks uue mudeli loomise asemel laadige varasemalt allalaaditud fail 1099model.xml. See fail sisaldab hankijakannete kohandatud andmemudelit. See andmemudel on vastendatud andmekomponentidega, mis on AOT andmemudelis.   

3. Klõpsake nuppu Vahetus.
4. Klõpsake nuppu Laadi XML-failist.

    Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini 1099model.xml.  

5. Klõpsake nuppu OK.
6. Puuvaates valige „1099 maksete mudel”.

## <a name="review-data-model-settings"></a>Andmemudeli sätete ülevaatamine
1. Klõpsake valikut Kujundaja.

    See mudel on mõeldud tähistama hankijate kandeid ettevõtte seisukohalt ja ei kuulu juurutamisesse.   

2. Puuvaates laiendage valikut „1099-MISC”.
3. Puuvaates valige nupp „1099-MISC\Kanded”
4. Puuvaates laiendage valikut „1099-MISC\Kanded”.

    Selle mudeli element Kanded tähistab individuaalseid kandeid. Tütarelemente kasutatakse iga kande jaoks vajalike üksikasjade määramiseks, nagu hankijakonto ja kande kuupäev.   

5. Sulgege leht.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Uue andmete importimist toetava elektroonilise aruandluse vormingu konfiguratsiooni lisamine
Selles alamülesandes olevad juhised näitavad teile, kuidas saab luua uue vormingu konfiguratsiooni, et hallata andmete importi välistest failidest.   
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Väljale Uus sisestage „Andmemudeli 1099 maksete mudelil põhinev vorming”.
3. Väljal Toetab andmeimporti valige Jah.
4. Selle lehekülje sulgemiseks vajutage klahvi ESC.

    Andmeimpordi toetamiseks uue vormingu loomise asemel laadige varasemalt allalaaditud fail 1099format.xml. See fail sisaldab imporditava faili määratletud struktuuri ja struktuuri vastendamist hankijakannete kohandatud andmemudeli järgi.   
5. Klõpsake nuppu Vahetus.
6. Klõpsake nuppu Laadi XML-failist.
    Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini 1099format.xml.  
7. Klõpsake nuppu OK.
8. Puuvaates laiendage valikut „1099 maksete mudel”.
9. Puuvaates valige „1099 maksete mudel \ Vorming hankijakannete importimiseks”.

## <a name="review-format-settings"></a>Vormingu sätete ülevaatamine
1. Klõpsake valikut Kujundaja.
2. Lülitage nupp Kuva üksikasjad sisse.
3. Klõpsake nuppu Laienda/ahenda.
4. Klõpsake nuppu Laienda/ahenda.

    Kujundatud vorming tähistab välise faili eeldatavat struktuuri. See fail peab olema XML-vormingus ja sellel peab olema tasakaalustuse juurelement. Iga hankijakannet tähistatakse kandeelemendiga, mis on määratletud kui nullist mitmeni mitmekordsuse olemasoluga. See tähendab, et sissetulev fail võib sisaldada nullist kuni mitme kandeni ükskõik mis arvu. „Kande” elemendi pesastatud elemendid tähistavad ühe kande atribuute. Pange tähele, et kõik atribuudid, välja arvatud riik, on tähistatud kohustuslikuks, mis tähendab, et nende olemasolu faili importimisel on kohustuslik.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Vaadake üle vormingu andmemudeliga vastendamise sätted
1. Klõpsake nuppu Vormingu vastendamine mudeliga.

    Vastendus „Hankijakannete importimiseks” sisaldab andmete ülekandereegleid sissetulevast XML-failist kohandatud andmemudeli valitud osani, mis on määratletud the1099-MISC määratluse valimisega.  

2. Klõpsake valikut Kujundaja.
3. Lülitage nupp Kuva üksikasjad sisse.
4. Puuvaates laiendage valikut „vorming: Kirje”.
5. Puuvaates valige „vorming: Kirje”.

    Pange tähele, et kujundatud vormingut tähistatakse siin andmeallika komponendina.  

6. Laiendage puul valikut `format: Record\*settlement: XML Element 1..1 (settlement): Record`.
7. Laiendage puul valikut `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`.
8. Laiendage puul valikut `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.
9. Laiendage puul valikut `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`.
10. Valige puul suvand `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.

    Pange tähele, et kohustuslike ja valikuliste vorminguelementide esitlus erineb eelmääratletud „vorminguga” andmeallika komponendist.  
11. Puuvaates laiendage „Kanded: Kirjete loend = format.settlement.'$enumerated”.

    Pange tähele, et imporditud faili struktuuri määratleva vormingu elemendid on seotud kohandatud andmemudeli elementidega. Nende sidumiste põhjal salvestatakse imporditud XML-fail käitusajal olemasolevasse andmemudelisse. Pöörake tähelepanu riigielemendi sidumisele. Sissetulevas failis, millel pole sellist elementi, täidetakse mis tahes kande elemendi puhul vaikimisi riigikood „USA” andmemudelis.  

12. Klõpsake vahekaarti Kinnitused.

    See vormingu vastendamine võib sisaldada kasutaja määratud loogikat, et kinnitada imporditud andmete täpsust ettevõtte seisukohalt. Näiteks sätte põhjal luuakse mis tahes ilma määratletud riigikoodita importimisfaili kande puhul teabelogis hoiatusteade, mis teavitab kasutajat juhtumi osas ja näitab kande seerianumbrit.  

13. Sulgege leht.

## <a name="run-the-format-mapping-to-the-data-model"></a>Vormingu andmemudeliga vastendamise käivitamine
Käivitage selle vormingu vastendamine testimisotstarbel. Kasutage varsemalt allalaaditud faili 1099entries.xml. Saate eksportida selle faili töövihikust 1099entries.xlsx, mida kasutatakse hankijakannete haldamiseks. Loodud väljund imporditakse valitud XML-failist ja täidetakse reaalsel importimisel kohandatud andmemudeliga.  

1. Klõpsake nuppu Käivita.

    Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini 1099entries.xml.  

2. Klõpsake nuppu OK.

    Pange tähele hoiatusteadet imporditud failis kande puhul puuduva riigikoodi kohta.  
    
    Vaadake väljund üle XML-vormingus, mis tähistab valitud failist imporditud ja andmemudelisse porditud andmeid.   

3. Sulgege leht.
4. Sulgege leht.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Vaadake üle mudeli sihtkohtadega vastendamise sätted
1. Puuvaates valige „1099 maksete mudel”.
2. Klõpsake valikut Kujundaja.
3. Klõpsake suvandit Mudeli vastendamine andmeallikaga.

    Impordi Manuaalsed 1099 kanded vastendamine on määratletud suunatüübiga Sihtkohani. See tähendab, et see on sisestatud andmeimpordi toetamiseks ja sisaldab reeglite sätet, mis määratleb, kuidas imporditud ja abstraktse andmemudeli andmetena kasutatavat välist faili kasutatakse tabelite värskendamiseks.  

4. Klõpsake valikut Kujundaja.
5. Puuvaates laiendage valikut „Andmemudeli 1099 maksete mudel”.
6. Laiendage puuvaates valikut 'mudel: Andmemudeli 1099 maksete mudel\Kanded: Kirjete loend”.

    Pange tähele, et kujundatud mudelit tähistatakse siin andmeallika elemendina. Käitusajal sisaldab see välisest failist imporditud andmeid. Mitu tabelit lisati andmeallika elemendina tagamaks, et imporditud andmed vastavad praeguse rakenduse andmetele, sealhulgas ka see, kas importimiskande hankijakonto on süsteemis saadaval, kas imporditavade riigi- ja osariigikoodide kombinatsioon on olemas jne.  

7. Puuvaates valige „model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean“.
8. Klõpsake nuppu Redigeeri.
9. Klõpsake suvandit Muuda valemit.

    Kui ühe imporditava kande puhul nurjub vähemalt üks kinnitamine, tähistatakse see kande andmeallika atribuudiga „$failed” nurjunuks.  

10. Sulgege leht.
11. Klõpsake valikut Tühista.
12. Puuvaates valige „tax1099trans: tabeli „VendSettlementTax1099” kirjed = model.Validated”.
13. Klõpsake nuppu Redigeeri sihtkoha.

    Lisati elektroonilise aruandluse sihtkoht, et määrata, kuidas imporditud andmed värskendavad rakenduse tabeleid. Sellisel juhul on valitud andmetabel VendSettlementTax1099. Kuna valitud on kirje toiming Lisa, sisestatakse imporditud kanded tabelisse VendSettlementTax1099. Pange tähele, et üksik mudeli vastendamine võib sisaldada mitut sihtkohta. See tähendab, et imporditud andmeid saab kasutada korraga mitme rakenduse tabelite värskendamiseks. Tabeleid, vaateid ja andmeolemeid saab kasutada elektroonilise aruandluse sihtkohtadena.   

    Kui vastendamist kutsutakse rakenduse punktist (nagu nupp või menüü-üksus), mis loodi spetsiaalselt sellele toimingule, tuleb elektroonilise aruandluse sihtkoht tähistada integratsioonipunktina. Selles näites on see punkt ERTableDestination#VendSettlementTax1099.  

14. Klõpsake valikut Tühista.
15. Klõpsake käsku Kuva kõik.
16. Klõpsake käsku Kuva ainult vastendatud.
17. Puuvaates laiendage valikut „tax1099trans: tabeli „VendSettlementTax1099” kirjed= model.Validated”.

    Pange tähele, et andmeallika element, mis sisaldab ainult kinnitatud kandeid, on seotud loodud sihtkohaga. Saate filtreerida imporditud kandeid, et jätta vahele need, mis vasta rakenduste andmetele.  

18. Puuvaates valige „nurjus: tabeli „VendSettlementTax1099Entity” kirjed = model.Failed”.
19. Klõpsake vahekaarti Kinnitused.

    See mudeli vastendamine võib sisaldada kasutaja määratud loogikat, et kinnitada imporditud andmete õigsust olemasolevatest rakenduse andmetest. Näiteks eelmääratud sätte põhjal luuakse mis tahes süsteemis mitteoleva hankijakontoga imporditud failis oleva kande puhul hoiatusteade, mis teavitab kasutajat ja näitab väära hankijakonto koodi.  

    Pange tähele, et suvandit Kontrollimisjärgne tegevus saab kasutada iga kinnitamise puhul, et määrata, kas importimisprotsessi tuleb jätkata või see katkestada, aga ka seda, kas juba tehtud sisestusi/värskendusi saab säilitada või pöörata tagasi.  

20. Klõpsake käsku Kuva ainult vastendatud.
21. Klõpsake käsku Kuva kõik.
22. Sulgege leht.

    Käivitage see mudeli vastendamine, et testida kujundatud vormingut ja mudeli vastendusi. Kasutage faili 1099entries.xml. Valitud failis sisalduvad andmed imporditakse süsteemi.  

23. Klõpsake nuppu Käivita.

    Pange tähele, et dialoogiboks ei sisalda täiendavaid küsimusi vormingu vastendamise kohta, mida tuleb kasutada imporditud faili sõelumiseks ja seejärel andmete portimiseks andmemudelisse. Seda seetõttu, et parajasti on ainult üks seda mudelit kasutavat vormingut, mis on tähistatud andmeimporti toetama.  
    
    Määratlege kande ID, et eristada imporditud kandeid teistest kannetest, mis võivad olla juba käsitsi sisestatud või imporditud.  

24. Väljale Kande ID sisestamine tippige „IMPORT-001”.

    Sirvige, et saada fail „1099entries.xml”.  

25. Klõpsake nuppu OK.

    Koostatud hoiatuste loend annab teavet valede hankijakontode, vale maksu 1099 kastikoodi, puuduvate riigikoodide jm kohta. Võrrelge seda loendit käivitamise XML-faili sisuga.  

26. Sulgege leht.
27. Sulgege leht.
28. Sulgege leht.
29. Sulgege leht.
30. Avage Ostureskonto > Perioodilised ülesanded > Maksu 1099 > Hankija tasakaalustus 1099 jaoks.

    See vorm näitab tabelis Tax1099Summary olevaid kumulatiivseid kandeid, mis on loodud imporditud kannete põhjal.  

31. Määrake väljal Alguskuupäev kuupäevaks 2000/01/01.
32. Klõpsake nuppu Manuaalsed 1099 kanded.

    See vorm sisaldab käsitsi lisatud ja äsja imporditud kannete loendit.  

33. Avage filter Kande veerg.
34. Sisestage filtri väärtus „IMPORT-001” väljale „Kanne”, kasutades filtri tehtemärki „algab väärtusega”.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Vaadake üle mudeli ja vormingu vastenduste vahelised seosed
1. Sulgege leht.
2. Sulgege leht.
3. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
4. Klõpsake valikut Aruandluse konfiguratsioonid.
5. Puuvaates valige „1099 maksete mudel”.

    Oletame, et soovite toetada samade andmete importimist, kuid TXT-faili vormingus.   

6. Dialoogiboksi avamiseks klõpsake nuppu Loo konfiguratsioon. 
7. Väljale Uus sisestage „Andmemudeli 1099 maksete mudelil põhinev vorming”.
8. Väljale Nimi tippige „Impordi andmed TXT-failist”.
9. Väljal Toetab andmeimporti valige Jah.
10. Klõpsake Loo konfiguratsioon.
11. Klõpsake valikut Kujundaja.
12. Klõpsake nuppu Vormingu vastendamine mudeliga.
13. Klõpsake valikut Uus.
14. Sisestage või valige väärtus väljal Määratlused.

    Valige suvand „1099-MISC”.  

15. Väljale Nimi tippige „Impordi andmed TXT-failist”.
16. Väljale Kirjeldus tippige „Impordi andmed TXT-failist”.
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.
19. Sulgege leht.
20. Klõpsake nuppu Redigeeri.

    Kui installisite kiirparanduse „KB 4012871 GER-i mudeli vastenduste tugi eraldi konfiguratsioonides võimalusega määrata erinevat tüüpi eeltingimused nende juurutamiseks erinevates rakenduse Dynamics 365 Finance versioonides” ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), käivitage sisestatud vormingu konfiguratsiooni puhul järgmine etapp „Lülita lipp Mudelivastenduse vaikeväärtus sisse”. Vastasel juhul jätke järgmine etapp vahele.  

21. Väljal Mudelivastenduse vaikeväärtus valige Jah.
22. Puuvaates valige „1099 maksete mudel”.
23. Klõpsake valikut Kujundaja.
24. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
25. Klõpsake nuppu Käivita.

    Kui installisite kiirparanduse „KB 4012871 GER-i mudeli vastenduste tugi eraldi konfiguratsioonides võimalusega määrata erinevat tüüpi eeltingimused nende juurutamiseks erinevates versioonides ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), valige otsinguväljal eelistatud mudelivastendus. Kui te pole kiirparandust veel installinud, jätke järgmine etapp vahele, kuna vastendus on vaikevormingu konfiguratsiooniga juba valitud.  
    
    Kui te pole veel kiirparandust KB 4012871 installinud, pange tähele, et dialoogiboks sisaldab täiendavat mudeli vastendamise küsimust, mida kasutatakse imporditava faili sõelumiseks. Andmed imporditakse seejärel dialoogiboksist andmemudelisse. Praegu saate valida, millist vormingu vastendust tuleb kasutada, sõltuvalt sellest, millist tüüpi faili plaanite importida.  
    
    Kui plaanite selle mudelivastenduse kutsuda rakenduse punktist, mis on spetsiaalselt ette nähtud selle toimingu jaoks, tuleb elektroonilise aruandluse sihtkoha ja vormingu vastendus märkida integratsiooni osaks.  

26. Klõpsake valikut Tühista.
27. Sulgege leht.
28. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
