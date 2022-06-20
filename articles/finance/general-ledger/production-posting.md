---
title: Tootmistellimuse sisestamine
description: See artikkel annab teavet erinevat tüüpi tootmistellimuse sisestamise kohta.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d41725325a82b24c1e5aa6bd2c1a5322f3078ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879620"
---
# <a name="production-postings"></a>Tootmise sisestused

See artikkel annab teavet erinevat tüüpi sisestuste kohta tootmistellimuse protsessis.


## <a name="material-consumption"></a>Materjali tarbimine

Materjalid registreeritakse tootmisel tarbituteks, kui sisestatakse tootmise komplekteerimise tööleht. See loob kanded, mis arvavad vaba kaubavaru maha. **Tootmise parameetrites saate** määrata, kas pooleliv toormaterjalide väärtus (nimetatakse LÕPETAmata toodanguks) tuleks sisestada pearaamatusse.

Lõpetamata toodangu (WIP) **·** **väärtus sisestatakse tarbitud materjalide hinnangulise omahinna ja tarbitud materjalide hinnangulise omahinna, lõpetamata toodangu kontodele.** Tootmistellimuse komplekteerimislehe protsess on tootmistellimusega seotud laokannete füüsiline uuendamine. Kui tootmistellimus registreeritakse lõpetatuna, tühistatakse füüsilised kanded ja seotud laokanded finantsiliselt uuendatakse. Kui lõpetav tööleht on sisestatud, kasutatakse **·** **tarbitud materjalide kulu ja tarbitud materjalide kulu, kasutatakse WIP** sisestamistüüpe.

Vahekaart **Tootmine** lehel Lao sisestusreeglid **kontrollib**, kuidas tootmistellimused pearaamatusse sisestavad. Seda kasutatakse, kui pearaamatu **sisestamisväljaks** **·** **on** lehel Tootmise juhtimise parameetrid määratud kas **Kaup ja ressurss või Kaup ja** kategooria. 

Komplekteerimislehe töölehe jaoks tootmistellimuse pearaamatusse sisestamiseks peavad järgmised tingimused olema täidetud:

-   Tootmise **juhtimise parameetrite lehel** peab olema valitud märkeruut **Sisesta komplekteerimisleht pearaamatusse**. Selle sätte saab alistada konkreetse saidi puhul tootmise juhtimise **parameetrites saidi lehel**.
-   Füüsilise **laovaru sisestamise** märkeruut peab ostutellimuse **real** valitud kauba puhul olema kauba mudeligruppide lehel märgitud.
-   Lao sisestusreeglite lehel tuleb määrata **põhikontod** järgmiste sisestustüüpide jaoks:
    -   **Tarbitud materjalide eeldatav omahind**
    -   **Tarbitud materjalide eeldatav omahind, WIP**

## <a name="time-consumption"></a>ajatarbimine.

Aeg, millal töötajad tootmistöödele kulutavad, salvestatakse **protsessikaardi töölehele** või töökaardi **töölehele**. Kui need töölehed on sisestatud, töödeldakse pearaamatu sisestus sihtotstarbelisele kontole lõpetamata toodangu (WIP) jaoks. See sisestus näitab tootmistellimusele kulutatud aja väärtust. Kui tootmistellimus on registreeritud lõpetatuks, tasakaalustatakse WIP-kontod.

Ajatarbimise sisestamiseks on kolm võimalust, sõltuvalt valikust, mis **on** **valitud väljal Pearaamatu sisestamine lehel Tootmise juhtimise parameetrid.**

## <a name="reporting-finished-goods-and-error-quantities"></a>Lõpetatud kaupade ja vigaste koguste aruandlus

Kui tootmistellimus on lõpetatuna **kinnitatud**, uuendatakse lõpetatud kaubad laos lõpetatuna kinnitatud **töölehe** kaudu. Kui kasutate lõpetamata toodangu raamatupidamist, sisestatakse pearaamatu tööleht lõpetamata toodangu kontode vähendamiseks ja lõpetatud kaupade lao suurendamiseks. Tööleht kasutab toote jaoks määratletud standardkulusid. Kui tootmise **juhtimise parameetrite lehel** on **valitud** suvand Kasuta hinnangulist omahinda, kasutatakse tootmistellimuse eeldatavaid kulusid.

Lõpetamata toodangu (WIP) **·** **väärtus sisestatakse hinnangulise tootmiskulu ja hinnangulise toodetud kulu, WIP-kontodele.** **Tootmistellimuse lõpetatuna** kinnitatud protsess on tootmistellimusega seotud laokannete füüsiline uuendamine. Kui tootmistellimus on lõpetatud, tühistatakse füüsilised kanded ja seotud laokanded finantsiliselt uuendatakse. Kui lõpetav tööleht on sisestatud, kasutatakse Toodetud **kulu ja** **Toodetud kulu, Lõpetamata toodangu** sisestamistüüpe.

Vahekaardil **Tootmine** lehel Lao **sisestusreeglid** saate kontrollida, kuidas tootmistellimused pearaamatusse sisestada. Seda kasutatakse, kui pearaamatu **sisestamisväljaks** **·** **on** lehel Tootmise juhtimise parameetrid määratud kas **Kaup ja ressurss või Kaup ja** kategooria. Kui **välja väärtuseks** on **seatud** Tootmisgrupid, saab tootmisgruppide lehe pearaamatu kaupade kiirkaarti kasutada ka tootmistellimuste sisestamise **juhtimiseks**.

Töölehe Lõpetatuna **kinnitatud** sisestamiseks tootmistellimuse pearaamatusse peavad olema täidetud järgmised tingimused:
-   Tootmise **juhtimise parameetrite lehel tuleb** valida märkeruut **Sisesta lõpetatuna pearaamatus**. Selle sätte saab alistada konkreetse saidi puhul tootmise juhtimise **parameetrites saidi lehel**.
-   Füüsilise **laovaru sisestamise** märkeruut peab ostutellimuse **real** valitud kauba puhul olema kauba mudeligruppide lehel märgitud.
-   Lao sisestusreeglite lehel tuleb määrata **põhikontod** järgmiste sisestustüüpide jaoks:
    -   **Eeldatav tootmiskulu**
    -   **Eeldatav tootmiskulu, WIP**

## <a name="ending-the-production-order"></a>Tootmistellimuse lõpetamine

Enne tootmistellimuse lõpetamist arvutatakse toodetud kogusele tegelikud kulud. Kõik hinnangulised materjali- töö ja üldkulud tühistatakse ja asendatakse tegeliku kuluga. Lõpetatud kauba kogukulu debiteeritakse **toodetud** **kulu kontolt ja krediteeritakse toodetud kulu, WIP konto kreeditis.** Tootmistellimuse ajal tarbitud materjalid **krediteeritakse** tarbitud materjalide kulu kreeditis ja debiteeritakse **materjalikulu, WIP konto** deebetis.

Kui valite **kulukalkulatsiooni** käivitamisel märkeruudu Lõpeta töö, muudetakse tootmistellimuse olekuks **Lõpetatud**. See olek takistab lisakulude tahtmatut sisestamist lõpetatud tootmistellimusele. Saate määrata, et lõpetatuna kinnitatud veakoguste väärtus tuleb eraldada lõpetatuna kinnitatud headele kogustele. Võite ka määrata veakoguste väärtuse sisestamise sihtotstarbelisele praagikontole. 

Kindla praagikonto määramiseks järgige neid samme.
1.  Minge tootmise **juhtimise seadistuse** > **·** > **tootmisjuhtimise parameetritele**.
2.  Valige vahekaart **Standardne** uuendamine.
3.  Väljal Praakmeetod **valige** praagikonto **·**.
4.  Valige väljal **Praakkonto** põhikonto, kuhu tuleks tootmistellimuse lõpetades sisestada veakoguse praak. Valige näiteks kulukonto, nt kulukonto 510380: tootmise praak.

Tootmistellimuse pearaamatusse sisestamiseks peavad lõpptöölehe jaoks olema täidetud järgmised tingimused:
-   Põhikontod peavad olema määratud lehel Varude **sisestusreeglid** või **Tootmisgrupid** järgmiste sisestustüüpide jaoks:
    -   **Tarbitud materjalide omahind**
    -   **Tarbitud materjalide omahind, WIP**
    -   **Toodangu omahind**
    -   **Toodangu omahind, WIP**
-   Kulukategooriate, ressursside või ressursigruppide **lehel** **tuleb** määrata **põhikontod** järgmiste tüüpide puhul:
    -   **Toodetud kulu– ja kulu**
    -   **Tarbitud toodangu omahind, WIP**

## <a name="indirect-costs-for-production-orders"></a>Tootmistellimuste kaudsed kulud

Kui töötlete tootmistellimuse kandeid, saate konfigureerida kaudsed kulud üldkulude või lisatasude hõivamiseks pearaamatus. Kaudsete kulude füüsilised kanded tuvastatakse laos komplekteerimislehe töölehe sisestamisel või lõpetatuna kinnitatud töölehel. Kaudsete kulude finantskandeid tuvastatakse laos lõputöölehe sisestamisel.

Saate tuvastada oma ajatarbimise kaudseid kulusid, mis on seotud **protsessikaardi** töölehtede või töökaardi **töölehtedega**. Need kanded tühistatakse ja sisestatakse finantskontodele tootmistellimuse lõpetamisel. Lisateabe saamiseks minge [kululehtedele](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Pearaamatusse sisestamise taseme juhtimine

**Tootmise juhtimise parameetrite lehel** saate kasutada välja **Pearaamatu sisestus**, et seadistada tootmisprotsesside pearaamatusse sisestamise tase. 

Saadaval on järgmised väljad.

### <a name="item-and-resource"></a>Kaup ja ressurss

Kui valite **suvandi Kaup ja** ressurss pearaamatu **sisestusväljal**, tulevad sisestuskontod protsessi toimingu ressursist või ressursigrupist. Esimeseks sisestusssuvandiks on kindla ressursi kontod. Kui kontot ei määrata, kasutatakse ressursigrupis määratud kontosid. Protsessi igal toimingureal võib olla kuluarvestuse ressursina **määratud üks ressurss**. Seda ressurssi kasutatakse kasutatava konto määramiseks. Seda valikut kasutatakse tavaliselt siis, kui organisatsioon määrab ressurssidele tegevuskulud. Ressursside puhul on kulud sageli kõrgemad ja nende abil saab langetada otsuseid "tee vs. ost". See on kõige üksikasjalikum sisestamiskonfiguratsioon ja võimaldab kõige detailseimat tootmisprotsessi sisestuste ja väga üksikasjaliku analüüsi.

### <a name="item-and-category"></a>Kaup ja kategooria

Kui valite **pearaamatu sisestusväljal** **suvandi** Kaup ja kategooria, tulevad sisestuskontod kulukategooria **leheküljelt,** mis on seotud protsessi iga reaga. Igal protsessi operatsioonireal võib olla kolm kulukategooriat: **seadistusaeg**, **käitusaeg** ja **kogus**. Seda valikut kasutatakse tavaliselt siis, kui teie organisatsiooni põhi fookus on protsessi tõhususele ja tegevuse kestusele. See valik on rohkem summeeritud sisestuste viis ja võimaldab siiski grupeerida kulusid kategooriatesse.

### <a name="production-group"></a>Tootmisgrupp

Kui valite suvandi **Tootmisgrupid** väljal **Pearaamatu sisestamine**, tulevad sisestuskontod leheküljelt **Tootmisgrupid**. **Tootmisgruppe** kasutatakse tavaliselt siis, kui enam kui üks tootmisrida käitab sarnaseid tooteid või omab sarnaseid seadmeid. Selle valiku abil saate võrrelda kahe erineva tootmisgrupi kulusid.  
  
> [!NOTE]
> Kui kasutatakse lõpetatud kauba kulu arvutamise standardmeetodit, kajastavad seda lõppkanded. Kui standardsel meetodil arvutatud tegelikud kulud ja kulud erinevad, sisestatakse erinevused kontole, mis näitab kasumit või kahjumit.

### <a name="route-groups-and-ledger-posting"></a>Protsessigrupid ja pearaamatu sisestamine

Protsessi igal operatsioonireal on määratud **protsessigrupp**. Grupi **Hinnang ja kuluarvestus protsessigrupi seadistusaega,** **·** **·** **·** **·** **·** **käitusaega ja kogust kasutatakse tootmistellimusele töökaardi või protsessikaardi töölehe sisestamisel kuluarvestuse aja arvestuse hindamiseks.** Kui valikud on keelatud, siis ajatarbimise kohta pearaamatusse kannet ei looda.

Protsessikaardi **või** töökaardi **töölehe** jaoks tootmistellimuse pearaamatusse sisestamiseks peavad olema täidetud järgmised tingimused:

-   Väli **Seadistusaeg**, **Käitusaeg** **või** Kogus peab olema valitud **leheküljel Protsessigrupp** grupp Hinnang **ja omahind**.
-   Järgmiste sisestustüüpide puhul tuleb põhikontod **määrata** kas **·** **kulukategooria**, protsessi, **protsessigrupi** või tootmisgruppide lehel:
    -   Eeldatav absorbeeritud tootmiskulu
    -   Tarbitud toodangu eeldatav omahind, WIP

Järgmine diagramm näitab protsessigrupi suhet iga operatsiooni (protsessirea) kogukulu arvutamisega antud protsessis. Igal protsessireal on üks protsessigrupp. Protsessigrupp kontrollib seadistusaja, käitusaja ja koguse parameetreid. Kulukategooria vahekaardil on kolm protsessigruppide **sättel** **põhinevat** seadistust, **käivitamist** ja kogust.**·** Kiirkaardil **Ajastus** on kolm välja, mis põhinevad protsessigrupil.

Kasutatav valem põhineb sellel, kas suvand on protsessigrupis lubatud. Valitud kulukategooria kulu korrutatakse kogusega, mis sisestati kogukulu arvutamise ajastusse.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Protsessigruppide suhe arvutatud kogukuluga.":::
Protsessigruppide suhe arvutatud kogukuluga. Igal protsessireal on üks protsessigrupp. Protsessigrupp kontrollib seadistusaja, käitusaja ja koguse parameetreid. Kulukategooria vahekaardil on kolm protsessigruppide sättel põhinevat seadistuse, käituse ja koguse valikut. Kiirkaardil Ajastus on kolm välja, mis on protsessigrupi alusel lubatud ja omahinnaga arveldatud. Kasutatav valem põhineb suvandi lubamisel protsessigrupis. Valitud kulukategooria kulu korrutatakse kogusega, mis sisestatakse ajastusse kogukulu arvutamiseks.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Sisestusprofiili näidiskonfiguratsioon

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid koos näidis põhikontode ja kirjeldustega. 

 - Veerg **Deebet/Kreedit** näitab, kas kanne on tavaliselt Deebet või Kreedit või mõnel juhul saab seda sisestada. 
 - Kliiringukonto **veerg** näitab, kas sisestamistüüp on kliiringukonto. Kontole sisestatud summa tühistatakse hilisema kande sisestamisel automaatselt. 
 - Veerg **P/F näitab** füüsilise sisestamise **P-d** ja finantsilist **sisestamist** F. 
 - Veerg **Järgi** näitab, kas kindla sisestustüübi põhikonto on tavaliselt sama mis mõni muu sisestamistüüp. Veeru väärtus näitab tavaliselt järgitud sisestamistüüpi.

> [!NOTE]
> Soovitatud põhikontod ja põhikonto nimed on soovitusliked. Soovitame teil teha koostööd raamatupidajaga, et määratleda ärivajaduste jaoks parim konfiguratsioon.


| Sisestamistüüp  | Põhikonto näide | Põhikonto nime näide| Konto tüüp | Deebet/kreedit? | Kliiringukonto | Füüsiline või finants | Järgige | Kirjeldus |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Tarbitud materjalide eeldatav omahind      | 140100               | Materjalide laoseis        | Vara        | Krediit         | Y                | P                     | Tarbitud materjalide omahind                | Seda kontot kasutatakse tootmistellimuse komplekteerimislehe töölehe sisestamisel. Selle konto vastaskonto on Materjalide, WIP-i eeldatav omahind. Selle konto summa tühistatakse tootmistellimuse lõpetades automaatselt. See konto tähistab bilansikontot.       |
| Tarbitud materjalide eeldatav omahind, WIP | 150150               | Tootmise lõpetamata toodang - materjalid | Vara        | Deebet          | Y                | P                     | Eeldatav tootmiskulu, WIP          | Seda kontot kasutatakse tootmistellimuse komplekteerimislehe töölehe sisestamisel. Selle konto vastaskonto on tarbitud materjalide eeldatav omahind. Selle konto summa tühistatakse tootmistellimuse lõpetades automaatselt. See konto tähistab lõpetamata toodangut teie bilansis.                  |
| Eeldatav tootmiskulu               | 140200               | Lõpetatud kaupade laoseis   | Vara        | Deebet          | Y                | P                     | Toodangu omahind                         | Seda kontot kasutatakse tootmistellimuse lõpetatuna kinnitatud töölehe sisestamisel. Selle konto vastaskonto on hinnanguline tootmiskulu, wip. Selle konto summa tühistatakse tootmistellimuse lõpetades automaatselt. See konto tähistab bilansikontot. |
| Eeldatav tootmiskulu, WIP          | 150150               | Tootmise lõpetamata toodang - materjalid | Vara        | Krediit         | Y                | P                     | Toodangu omahind, WIP                    | Seda kontot kasutatakse tootmistellimuse lõpetatuna kinnitatud töölehe sisestamisel. Selle konto vastaskonto on hinnanguline tootmiskulu. Selle konto summa tühistatakse tootmistellimuse lõpetades automaatselt. See konto tähistab lõpetamata toodangut teie bilansis.                     |
| Tarbitud materjalide omahind                | 140100               | Materjalide laoseis        | Vara        | Krediit         | E                 | R                     | Tarbitud materjalide eeldatav omahind      | Seda kontot kasutatakse tootmistellimuses lõpetamisprotsessi käigus tarbitud materjalide äratundmiseks. Selle konto vastaskonto on tarbitud materjalide kulu, WIP.                                                                                                    |
| Tarbitud materjalide omahind, WIP           | 150150               | Tootmise lõpetamata toodang - materjalid | Vara        | Deebet          | E                 | R                     | Tarbitud materjalide eeldatav omahind, WIP | Seda kontot kasutatakse lõpetamata toodangus materjalide äratundmiseks, mida tarbitakse tootmistellimuses lõpetamisprotsessi ajal. Selle konto vastaskonto on tarbitud materjalide kulu.                                                |
| Toodangu omahind                         | 140200               | Lõpetatud kaupade laoseis   | Vara        | Deebet          | E                 | R                     | Eeldatav tootmiskulu               | Seda kontot kasutatakse lõpetatud kauba kulu äratundmiseks, mille tootsite tootmistellimusega tootmistellimuse lõpetamisel. Selle konto vastaskonto on Toodetud kulu, WIP konto.                                                                  |
| Toodangu omahind, WIP                    | 150150               | Tootmise lõpetamata toodang - materjalid | Vara        | Krediit         | E                 | R                     | Eeldatav tootmiskulu, WIP          | Seda kontot kasutatakse lõpetatud kauba kulu äratundmiseks WIP-is, mis toodetakse tootmistellimusega tootmistellimuse lõpetamisel. Selle konto vastaskonto on toodetud kulukonto.                                     |

> [!NOTE]
> Kulusäästliku **teenuse lõpetamata toodangu** sissetuleku **ja kulusäästliku** teenuse lõpetamata toodangu kliiringukontot kasutatakse lean manufacturingi omahinna tagasiarvestusega. Lisateabe saamiseks minge omahinna [tagasiarvestuse juurde](/supply-chain/cost-management/backflush-costing.md).

