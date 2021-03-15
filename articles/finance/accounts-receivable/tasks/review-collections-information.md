---
title: Sissenõuete teabe ülevaatamine
description: Selles teemas selgitatakse, kuidas vaadata üle sissenõuete teavet ja eri häälestuse suvandeid ja sissenõuete kandeid.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbfb6537118a9936c127018427b0516e7ea002a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971524"
---
# <a name="review-collections-information"></a>Sissenõuete teabe ülevaatamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas vaadata üle sissenõuete teavet ja eri häälestuse suvandeid ja sissenõuete kandeid. See protsess kasutab demoettevõtte USMF-i andmeid.

## <a name="create-customer-pools"></a>Kliendikaustade loomine
1. Navigeerimispaanil minge **Modulid > Kreedit ja sissenõuded > Häälestus > Kliendikaustad**.
- Sellel lehel saate häälestada kliendikaustad, mis on päringud, mis määravad kliendikontode grupi, mida saab sissenõuete või aegumisprotsesside jaoks kuvada ja hallata. Kasutage kliendikaustasid teabe filtreerimiseks loendilehel **Sissenõuded** ja seotud loendilehtedel. Kliendikaustadega saate ka filtreerida kliendikontosid, mis kaasatakse aegumise hetktõmmiste loomisel.  
- Kliendikaustadega saate filtreerida kliendikontosid, mis kaasatakse aegumise hetktõmmiste loomisel.  
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Kausta ID**.
4. Sisestage väärtus väljale **Kausta kirjeldus**.
5. Klõpsake **Vali kausta kriteeriumid**.
6. Sisestage väärtus väljale **Kriteerium**.
7. Valige nupp **OK**.
8. Valige **Kliendikausta ülevaade**.

## <a name="create-collections-agents"></a>Inkassaatorite loomine
1. Navigeerimispaanil minge **Moodulid > Kreedit ja sissenõuded > Häälestus > Inkassaatorid**.  
- Sellel lehel saate määrata töötajaid inkassaatoriteks ja soovi korral määrata neile kliendikaustu. *Inkassaator* on isik, kes töötab klientidega, et kinnitada maksete õigeaegne kogumine.  
- Sellel lehel häälestatud inkassaatorid lisatakse automaatselt sissenõuete töörühma. Kui töörühm on valitud väljal **Töörühm** lehel **Müügireskontro parameetrid**, lisatakse inkassaatorid sellesse töörühma. Kui töörühm pole valitud, luuakse automaatselt uus töörühm nimega Sissenõuded ja inkassaatorid lisatakse sellesse rühma.  
2. Valige soovitud inkassaator ja seejärel valige lehel **Lisa**.
3. Väljal **Kausta ID** valige soovitud kirje ripploendi menüüs.
4. Valige või puhastage märkeruut **Vaikimisi kaust**.
- Tehke see valik kõigi kliendikaustade lisamiseks valitud inkassaatori filtriloenditesse. Kui seda valikut pole tehtud, on filtriloendites saadaval ainult sellele inkassaatorile määratud kliendikaustad.  

## <a name="create-aging-period-definition"></a>Aegumisperioodi määratluse loomine
1. Navigeerimispaanil minge **Moodulid > Kreedit ja sissenõuded > Häälestus > Aegumisperioodi definitsioonid**.
- Saate kasutada aegumisperioodi definitsioone kliendi- ja hankijakontode vanuse analüüsiks teie sisestatavate andmete alusel. Iga aegumisperioodi definitsiooni jaoks seadistatud aegumisperiood vastab analüüsi tegemise käigus loendilehel, vormis või aruandes olevale veerule.  
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Aegumisperioodi definitsioon**.
4. Sisestage väärtus väljale **Kirjeldus**.
- Määrake perioodi nimi, ühik ja iga aegumisperioodi intervalli aegumisperioodi määratlusse kaasamiseks. Nulliga (0) rida väljal Üksus näitab analüüsi käivitamiskuupäeva. Enne nulli olevatel ridadel on väljal Ühik vaikekirjeks –1 ning peale nulli olevatel on 1, kuid seda saab muuta. Valige **Üles** ja **Alla**, et ridu ümber paigutada. 0 (null)-rida ei saa muuta.  
- Liigutage kursor kohta, kuhu soovite lisada uue rea ja seejärel valige **Lisa**.  
- Valige inkassaator aegumisperioodi esindama vormil ja loendilehel **Sissenõudmised**. Näiteks võite valida praegusele perioodile rohelise indikaatori, viimase 30 päeva pikkusele perioodile kollase indikaatori ja viimase 90 päeva pikkusele perioodile punase indikaatori.  
- Valige aegumisperioodi määratluse printimissuund. See valik määrab veergude kuvamise järjekorra kliendi või hankija aegumisaruandes.  
  - Edasi: veerud prinditakse samas järjekorras, milles pealkirjad tabelis kuvatakse, alustades ülemisest reast.  
  - Tagasi: veerud prinditakse vastupidises järjekorras sellele, milles pealkirjad tabelis kuvatakse, alustades alumisest reast.    

## <a name="setup-collections-parameters"></a>Sissenõuete parameetrite seadistamine
1. Navigeerimispaanil minge **Moodulid > Kreedit ja sissenõuded > Häälestus > Müügireskontro parameetrid**.
2. Valige vahekaart **Sissenõuded**.
3. Laiendage või ahendage jaotis **Sissenõuete vaikesätted**.
- Valige aegumisperioodi definitsioon vaikimisi aegumise hetktõmmise jaoks, mida kasutatakse vormil **Sissenõuded**.  
- Valige töörühm, millele määratakse inkassaatorid vormil **Inkassaator**. Loendis kuvatakse ainult töörühmad, mille tüüp on Sissenõuded.  
4. Laiendage või ahendage jaotis **Mahakandmine**.
- Valige töölehe nimi, mis sätestatakse päevaste pearaamatute töölehtedeks, mida kasutatakse kui kanne kantakse maha, kasutades vormi **Sissenõuded** või seotud loendilehti.  
- Valige vaikimis põhjusekood, mida kasutatakse kannete mahakandmisel, mille loomiseks on kasutatud vormi **Sissenõuded** või seotud loendilehti.  
- Valige see suvand, et luua eraldi töölehe rida käibemaksu summade jaoks, kui kannete mahakandmise loomiseks on kasutatud vormi **Sissenõuded** või seotud loendilehti. Selle valiku puhul saate hõlpsasti jälgida käibemaksusummasid, mis on seotud mahakandmise kannetega. Saate jälgida käibemaksusummasid eraldi, et kohandada hõlpsamini vastava perioodi käibemaksukohust.  
5. Laiendage või ahendage jaotis **Meilisõnumi mall**.
- Valige meilisõnumi mall, mida kasutada, kui saadete meilisõnumi kasutades selleks **Meil > Kanded**, et siduda toiminguga vormil **Sissenõuded**.  
- Valige meilisõnumi mall, mida kasutada, kui saadate kliendile väljavõtte meilisõnumi manusena, kasutades selleks **Meil > Väljavõte**, et siduda toiming vormil **Sissenõuded**.  
- Valige meilisõnumi mall, mida kasutada, kui saadete meilisõnumi, kasutades selleks **Meil > Kanded**, et siduda müügiesindaja toiming vormil **Sissenõuded**.  

## <a name="age-customer-balance"></a>Kliendi saldo aegunuks märkimine
1. Navigeerimispaanil minge **Moodulid > Kreedit ja sissenõuded > Perioodilised ülesanded > Kliendi saldo ajaliselt jaotamine**.
- Valige aegumisperioodi definitsioon. Aegumise hetktõmmise töötlemine märgib kanded aegunuks vastavalt valitud aegumisperioodi määratluses määratletud aegumisperioodidele.  
- Valige kliendikaust või jätke see väli tühjaks aegumise hetktõmmise loomiseks kõigile klientidele. Kliendikausta valimisel rakendatakse aegumise hetktõmmise töötlemist ainult kliendikausta kuuluvatele kliendikontodele. Valitud kliendi kausta tüüp peab olema Aegumise hetktõmmis.  
- Valige kuupäeva tüüp, millel aegumise hetktõmmis põhineb.  
  - Kande kuupäev: iga kande aegumine põhineb selle kande kuupäeval.    
  - Tähtaeg: iga kande aegumine põhineb selle tähtajal.    
  - Dokumendi kuupäev: iga kande aegumine põhineb selle dokumendi kuupäeval.  
- Valige kuupäev, mida kasutada aegumise hetktõmmise praeguse kuupäevana. Aegumisperioodid arvutatakse selle kuupäeva alusel.    
  - Tänane kuupäev: kasutage süsteemi kuupäeva. Tehke see valik, kui töötlemine on seadistatud toimuma korduva partiina. Kui kasutate seda kuupäeva, saab korduvat partiid perioodiliselt käitada ja kasutatakse süsteemi kuupäeva sellel ajal.    
  - Valitud kuupäev: kasutage enda määratud kuupäeva. Selle valiku korral sisestage aegumiskuupäev.  
2. Valige nupp **OK**.

## <a name="view-aged-customer-balances"></a>Aegunud kliendi saldode vaatamine
1. NAvigeerimispaanil valige **Moodulid > Kreedit ja sissenõuded > Sissenõuded > Aegunud saldod**.
- Kasutage loendilehte kliendisaldode ja aegunud summade vaatamiseks aegumisperioodi järgi. See teave salvestatakse aegumise hetktõmmisesse. Aegumisperioodid on määratud kasutatava aegumisperioodi definitsiooniga. Aegumisperioodi definitsioon võetakse kliendikaustast, kui see on kaustale määratletud. Kui kliendikaustal ei ole aegumisperioodi definitsiooni, kasutatakse vormis Müügireskontro parameetrid määratud vaikimisi aegumisperioodi definitsiooni.  
2. Laiendage kiirinfo **Kontakt**. Siin saate vaadata kontaktteavet.
- Kliendi sissenõuete kontakt.  
- Kliendi vaikemüüja.  
3. Laiendage kiirinfot **Krediidilimiit**.
- Kasutage kiirinfot **Krediidi teave**, et kuvada kliendile krediidilimiit ja praegune bilansi info.  

## <a name="view-customer-collections-details"></a>Kliendi sissenõuete üksikasjade kuvamine
1. Veenduge, et soovitud kirje on valitud.
2. Laiendage kiirinfo **Aadress**, **Kontakt**, **Aegumine** ja **Krediidilimiit**, et kuvada valitud info.
3. Toimingupaanil valige **Kogu**.
- Uuendage kliendi aegumise hetktõmmist, kasutades tänast kuupäeva aegumiskuupäevana, millega kande kuupäevi võrreldakse. Kui aegumise hetktõmmis hõlmab mitme juriidilise isiku teavet, hõlmab uuendatud aegumise hetktõmmis samade juriidiliste isikute teavet. Summad talletatakse aegumise hetktõmmise uuendamise ajal sisselogitud juriidilise isiku arvestusvaluutas.  
- Valige aegumisperioodi definitsioon. Vaikimisi kuvatakse kliendi aegumise hetktõmmisega seostatud aegumisperioodi määratlus. Aegumisperioodi definitsioon kontrollib aegumisperioode ja hulkasid, mida näidatakse kiirinfos **Aegunud saldo** ja **Krediiditeave**.  
- Avage menüü, mis sisaldab järgmisi üksusi.    
  - Ettevõte – aegunud saldode ja krediiditeabe kiirinfo kuvamine juriidilise isiku arvestusvaluutas.  
  - Klient – aegunud saldode ja krediiditeabe kiirinfo kuvamine kliendi valuutas.  
- Valige kliendi aegumise hetktõmmises üks või mitu juriidilist isikut, kelle teavet soovite vaadata. Loendis olevad juriidilised isikud olid aegumise hetktõmmise loomisel valitud.  
- Kliendi väljavõtte kuvamine Microsoft Exceli vormingus. Saate valida kannete vahemiku alguskuupäeva, mis kaasatakse väljavõttesse, ja otsustada, kas soovite kaasata ainult avatud kanded või nii avatud kui ka tasakaalustatud kanded. Kui aegumise hetktõmmis hõlmab mitme juriidilise isiku teavet, kaasatakse kõigi juriidiliste isikute kanded.  
- Avage vorm **Dokumendid**, milles saate luua ja redigeerida dokumente või märkmeid.  
4. Toimingupaanil valige **Suhtle**.  
- Avage Outlook, kus saate saata meilisõnumi väljal Kontakt määratud kontaktile. Kui sissenõuete kontakt määramata, kasutatakse kliendi konto peamist aadressi. Kui peamist kontakti pole määratud, saadetakse meilisõnumid esimesena märgitud meiliaadressile vormil **Kontaktid**. Valitud kanded kaasatakse manustena. Manus on Exceli vormingus ja hõlmab kolme töölehte. Meilisõnumi malli kliendikontakti sõnumite jaoks saab täpsustada vormil **Müügireskontro parameetrid**.  
- Nupp ei ole saadaval, kui sellel vormil valitud kontakti meiliaadress on häälestamata.  
- Valmistage ette väljavõte ja avage Outlook, kus saate saata meilisõnumi, millele on lisatud manusena väljavõte, aadressile, mis on täpsustatud vormil **Kontakt**. Kui sissenõuete kontakt määramata, kasutatakse kliendi konto peamist aadressi. Kui peamist kontakti pole määratud, saadetakse meilisõnumid esimesena märgitud meiliaadressile vormil **Kontaktid**.  
- Nupp ei ole saadaval, kui sellel vormil valitud kontakti meiliaadress on häälestamata.  
- Avage Outlook, kus saate saata meilisõnumi kliendile määratud müügigrupi müügiesindajaks määratud töötajale. Kui kanded on valitud, kaasatakse need manustena. Manus on Exceli vormingus ja hõlmab kaht töölehte. Meilisõnumi malli müügiesindajate sõnumite jaoks saab täpsustada vormil **Müügireskontro parameetrid**.  
- Nupp ei ole saadaval, kui sellel vormil kuvatud müüja meiliaadress on häälestamata.  
- Saate kuvada kliendi kanded ja teha nendega seotud toiminguid. Tsentraliseeritud maksete kasutamisel kaasatakse kõigi kliendi aegumise hetktõmmises olevate juriidiliste isikute teave. Saate keelata juriidilise isiku teabe valides **Ettevõte** toiminguplaani rühmas **Vali**.  
- Muutke valitud kannete sissenõudeolekut.    
  - Vaidlustamata: kande puhul ei ole sissenõudetegevust toimunud.    
  - Vaidlustatud: klient on teid teavitanud kandega seotud probleemist.    
  - Lubatud maksta: klient on nõustunud maksma kandesumma.    
  - Lahendatud: kõik kande probleemid on lahendatud ja mingeid täiendavaid sissenõudmistegevusi ei ole vaja.  
- Avage menüü ja valige üks järgmistest üksustest, et täpsustada, milliseid kandeid soovide sellel vormil kuvada.    
  - Avatud – kuvatakse ainult tasakaalustamata kanded.    
  - Avatud ja suletud – kuvatakse kõik kanded, nii tasakaalustatud kui tasakaalustamata.  
- Töödelge valitud makset ebapiisavate vahendite (NSF) maksena.    
  - See nupp on saadaval ainult siis, kui valitud kanne on maksete töölehele sisestatud makse (arveta kreeditsaldo), kandele on määratud pangakonto ja makset ei ole varem tühistatud.  
- Kandke valitud kanded maha.  
- Märkige valitud kanded üksteisega tasakaalustamiseks.  
- Avage vorm **Algne dokument**, milles saate vaadata ja printida valitud kande dokumendi.  
- Avage **menüü**, mis sisaldab järgmiseid üksuseid.    
  - Sissenõuded – kuvab ainult neid toiminguid, mis on loodud sissenõudmiste vormil.    
  - Kõik – kõigi selle kliendi tegevuste kuvamine olenemata nende loomiskohast.  
- Avage **menüü**, mis sisaldab järgmiseid üksuseid.    
  - Avatud – kuvab ainult neid toiminguid, mis pole suletud.    
  - Avatud ja suletud – kõigi tegevuste kuvamine olenemata nende olekust.  
- Valige kliendile määratud sissenõuete juhtum või jätke väli tühjaks. Kui juhtum on valitud, kuvatakse vormil ainult selle juhtumiga seostatud kanded ja tegevused.  
5. Valige **Näita loendit**.
- Valige kliendi konto või nõustuge vaikesisestusega. Vaikimisi on see loendilehel või vormil, millelt avasite selle vormi, valitud kliendi konto. Kui avasite vormi loendilehelt, on loendis kliendid, kes on kaasatud loendilehel kasutatavasse kliendikausta.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]