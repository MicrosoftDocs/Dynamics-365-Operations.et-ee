---
title: Finantsaruande loomine
description: "See teema sisaldab finantsaruande koostamise üldteavet."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Finantsaruande loomine

[!include[banner](../includes/banner.md)]


See teema sisaldab finantsaruande koostamise üldteavet. 

Aruande loomiseks avage aruande definitsioon ja klõpsake seejärel tööriistaribal nuppu Loo. Avatakse aken Aruannete järjekorra olek ja näidatakse teie aruande asukohta järjekorras. Vaikimisi avaneb loodud aruanne veebivaaturis.
| ![Märkus](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Märkus")**Märkus**        |
|------------------------------------------------------------------------------------------------|
| Saate luua aruandeid ainult kaustadesse ja asukohtadesse, millele teil on juurdepääsuluba. |

Järgmises tabelis selgitatakse aruannete loomiseks saadaolevaid suvandeid.

| Suvand                                                                                | Lisateave |
|---------------------------------------------------------------------------------------|----------------------|
| Graafiku seadistamine aruande või aruannete grupi automaatseks loomiseks              |                      |
| Aruandest puuduvate kontode või andmete kontrollimine või aruande ja aruande täpsuse kinnitamine |                      |

Aruande loomisel kasutatakse valikuid, mille olete määranud valiku Aruande definitsioon vahekaartidel. Vahekaardil Väljund ja jaotus saate määrata aruandeteegi asukoha, mis võimaldab aruande lihtsat jagamist.

## <a name="schedule-report-generation"></a> Aruande graafiku loomine
Paljudel ettevõtetel on tuumik aruandeid, mida käivitatakse plaanitud ajavahemike järel äriprotsessidega kooskõlastamiseks. Saate plaanida aruande regulaarselt loomise, näiteks iga päev, nädal, kuu või aasta. Selleks võib olla üks aruanne või mitut ettevõtet hõlmav aruannete grupp. Peate sisestama mandaadid iga määratud (näiteks aruandluspuu definitsioonis) ettevõtte puhul. Kui mandaadid on kehtetud, kuvatakse aruandes ainult teave, millele teil on juurdepääsuõigus, nt ettevõte, kuhu olete sisse logitud. Väljundi teavet loetakse esmalt aruannete grupist ja seejärel üksikutest aruannetest.

Aruande graafikute loomisel ja salvestamisel kuvatakse need navigeerimispaanil suvandi Aruande graafikud all. Saate aruannete korraldamiseks luua kaustu. Kui graafiku üks aruanne ei käivitu, jätkatakse kõigi teiste aruannete käivitamist.
| ![Tähtis](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tähtis")**Tähtis**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aruande graafikute loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll. Aruande käivitamisel kasutatakse aruande loomiseks graafiku loonud kasutaja mandaate. |

### <a name="create-a-report-schedule"></a>Aruande graafiku loomine

1.  Klõpsake aruande kujundaja menüüs Fail nuppu Uus ja seejärel valige Aruande graafik. Avaneb dialoogiboks Uus aruandegraafik.
2.  Valige vahekaardilt Sätted plaanitav üksik aruanne või aruannete grupp. Saadaval on ainult aruanded või aruannete grupid ettevõtte või koosteüksuse puhul, millesse olete praegu sisse logitud.
3.  Aruande graafiku sisselülitamiseks valige märkeruut Aktiivne. Aruande graafiku saab aktiveerida või inaktiveerida vaid aruande looja või administraator.
4.  Ettevõtte mandaatide sisestamiseks klõpsake nuppu Load. Vaikimisi kasutatakse teie sisselogimisteavet ettevõtte puhul, millesse olete sisse logitud. Kui kaasatud on muud ettevõtted, näiteks aruandluspuu definitsioonides, valige suvand Kasuta eraldi mandaate ja seejärel sisestage mandaadid muu aruande graafikusse kaasatud ettevõtte puhul. Saate valida suvandi Windowsi autentimine või sisestada kasutajanime ja parooli iga ettevõtte puhul. Valige märkeruut Salvesta mandaadid nende ettevõtete mandaatide salvestamiseks ja seejärel klõpsake dialoogiboksi sulgemiseks nuppu OK.
5.  Valige suvandi Sagedus väljalt Korduse käivitamine kuupäev, mil graafik käivitatakse. Vaikimisi valitakse klientarvuti praegune süsteemikuupäev.
6.  Valige väljalt Käivita aruanne aeg, mil aruanne tuleks käivitada. Sisestades aja, mis on praegusest süsteemiajast varasem, käivitatakse aruanne järgmisel plaanitud kuupäeval.
7.  Määrake alal Kordumismuster, kui tihti aruanne käivitada. Vaikimisi valitakse Iga päev koos valiku Intervall (päevad) väärtusega 1. Muud valikud on Kord nädalas, Kord kuus ja Kord aastas.
8.  Valige alas Kordumisvahemik, millal tuleks aruande loomine lõpetada.
    -   Lõppkuupäev puudub – aruande graafikut käivitatakse määramata aja jooksul.
    -   Määratud esinemiste arv – aruande graafikut käivitatakse määratud arvu kordi ja seejärel inaktiveeritakse.
    -   Lõpeta – aruande graafik lõpeb määratud kuupäeval.

9.  Klõpsake tööriistaribal nuppu Salvesta. Sisestage dialoogiboksi Salvesta nimega aruande graafiku kordumatu nimi ja kirjeldus.

Aruande graafiku kopeerimiseks peab teil olema kujundaja või administraatori roll. Isegi kui administraator aruande graafikut muudab, säilitab aruanne aruande loonud kasutaja mandaate.
### <a name="copy-a-report-schedule"></a>Aruande graafiku kopeerimine

1.  Klõpsake aruande kujundajas navigeerimispaanil suvandit Aruande graafikud ja avage kopeeritav aruande graafik.
2.  Klõpsake menüüs Fail käsku Salvesta nimega ja seejärel sisestage graafiku kordumatu nimi ja kirjeldus dialoogiboksi Salvesta nimega. Klõpsake nuppu OK ja navigeerimispaanil kuvatakse uus graafik.
3.  Vajaduse korral muutke uues graafikus välju ja teavet ja seejärel klõpsake tööriistaribal nuppu Salvesta või klõpsake käsku Salvesta menüüs Fail.

Aruande graafiku kustutamiseks peate olema aruande graafiku omanik või teil peab olema administraatori roll.
### <a name="delete-a-report-schedule"></a>Aruande graafiku kustutamine

1.  Klõpsake aruande kujundajas navigeerimispaanil suvandit Aruandegraafikud.
2.  Valige kustutatav aruande graafik ja seejärel klõpsake suvandit Kustuta või vajutage klahvi Delete.
3.  Klõpsake kustutamise kinnitamise dialoogiboksis aruande graafiku jäädavalt kustutamiseks suvandit Jah. Kui teil pole õigust graafikut kustutada, kuvatakse teade ja aruannet ei kustutata.

### <a name="credentials-and-report-schedules"></a>Mandaadid ja aruande graafikud

Kui te ei sisesta kõikide aruandesse kaasatud ettevõtete puhul nõutavaid mandaate, kuvatakse aruande graafiku salvestamisel järgmine teade: „Peate sisestama mandaadid sellesse aruande graafikusse kaasatud ettevõtete puhul.” Valige oma mandaatide sisestamiseks nupp Load.

Näiteks Phyllis logib ettevõttesse A oma kasutajanime ja parooliga. Ta loob mitme ettevõtte andmete kogumiseks aruandluspuu definitsiooni kasutava aruande graafiku. Selle aruande graafiku salvestamisel viibatakse Phyllist sisestama mandaate teiste aruandluspuu definitsioonis määratletud ettevõtete puhul. Mandaatide aegumisel ei looda aruande graafikus olevaid mõjutatud aruandeid kuni mandaatide värskendamiseni. Lubade värskendamise viitamiseks kuvatakse aruannete järjekorras teade. Aruande graafik nurjub mis tahes järgmiste asjaolude korral (kuna need nõuavad mandaate).
-   Uus ettevõte on lisatud aruandluspuusse üksiku aruande puhul.
-   Aruandegrupi aruannet on muudetud.
-   Aruandegruppi on lisatud uus aruanne täiendava ettevõtte puhul.

Jätkamiseks klõpsake nuppu Load dialoogiboksis Aruande plaanimine ja seejärel sisestage sobivad mandaadid.

## <a name="missing-account-analysis-feature"></a> Puuduva konto analüüsi funktsioon
Saate otsida finantskontosid ja dimensioone, mis võivad olla puudu koosteüksuste grupi kõigis readefinitsioonides, aruandluspuu definitsioonides ja aruande definitsioonides. See on kasulik mitme konto või koosteüksuse loomisel või värskendamisel lühikese aja jooksul ja kui soovite kontrollida, kas kogu teave on aruannetesse kaasatud.

Puuduvad kontod määratakse, kasutades readefinitsiooni või aruandluspuu definitsiooni kõige madalamaid ja kõrgemaid väärtusi ja seejärel kuvatakse loend kontodest, mida pole readefinitsioonis või aruandluspuu definitsioonis, kuid on finantsandmetes. Kui puuduv konto on readefinitsiooni väärtustest suurem või väiksem, ei kaasata seda kontot puuduvate kontode loendisse.
| ![Näpunäide](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Näpunäide")**Näpunäide**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Kinnitamise eesmärgil tuleks see protsess käivitada enne igakuiste aruannete loomist ja uute koosteüksuste loomisel. |

Väärtuste vahemikega aruannete puhul on kontode puudumine vähem tõenäoline. Võimaluse korral kasutage koosteüksuse vahemikke uute kontode lisamiseks nende loomisel. Kui mis tahes aruande definitsioon on määratud ettevõttele @ANY, saate konkreetsesse ettevõttesse sisse logida ja selle ettevõtte puhul puuduva konto analüüsi käivitada.
| ![Märkus](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Märkus")**Märkus**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kui on lisatud uus ettevõte, peate lisama uue ettevõtte mis tahes olemasolevate aruannete aruandluspuudesse, vastasel korral ettevõtet puuduva konto analüüsi ei kaasata. |

### <a name="run-missing-account-analysis"></a>Puuduva konto analüüsi käivitamine

1.  Klõpsake aruande kujundajas suvandit Tööriistad ja seejärel klõpsake suvandit Puuduva konto analüüs.
2.  Valige väljalt Ettevõtte filter ettevõte, mille põhjal tulemusi filtrida või valige suvand Kõik (filter puudub) tulemuste kuvamiseks kõigilt saadaolevatelt ettevõtetelt.
3.  Valige väljalt Dimensioonifilter dimensioon, mille põhjal tulemusi filtrida või valige suvand Kõik (filter puudub) dimensiooniteabe kuvamiseks kõigi saadaolevate dimensioonide puhul.
4.  Valige väljalt Grupeerimisalus tulemuste sortimiseks suvand. Saate sortida tulemusi seotud koosteüksuse järgi või dimensiooni ja väärtuste kogumite alusel.
5.  Vaadake kuvatud tulemused üle. Üksuse valimisel ülemiselt paanilt kuvatakse alumisel paanil erandi teave. See hõlmab seotud dimensioone, väärtusi ja aruandeid.
6.  Seotud üksuse avamiseks klõpsake loendi paanil kuvatavat seotud ikooni või paremklõpsake üksust ja valige käsk Ava. Mitme üksuse valimiseks hoidke alumisel paanil üksuste valimisel all klahvi Ctrl.
7.  Mis tahes väärtuste, koosteüksuste või aruannete tagastamisel, mis ei tohiks aruandesse kaasatud olla, paremklõpsake üksust ja valige üksuse loendist eemaldamiseks käsk Välista või valige üksuse kõrval olev märkeruut Välista. Loendi värskendamisel välistatud üksusi ei kaasata. Mitme üksuse valimiseks hoidke alumisel paanil üksuste valimisel all klahvi Ctrl. Kõigi üksuste, sh eelnevalt analüüsist välistamiseks valitud mis tahes üksuste kuvamiseks valige märkeruut Kuva välistatud koosteüksused ja väärtused ja seejärel klõpsake käsku Värskenda.
8.  Osutatud erandite värskendamiseks klõpsake käsku Värskenda. Kõigi tulemuste täielikuks värskendamiseks klõpsake suvandit Jah või klõpsake osutatud üksuste osaliseks värskendamiseks suvandit Ei.
    | ![Märkus](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Märkus")**Märkus**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Vormi värskendatakse automaatselt selle avamisel, v.a juhul, kui vorm on olnud avatud viimased 15 minutit. |

9.  Probleemide lahendamisel klõpsake dialoogiboksi sulgemiseks nuppu OK.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Kiirklahvid puuduva konto analüüsi puhul
Puuduva konto analüüsi käivitamisel on saadaval järgmised kiirklahvid.

| Toiming                           | Kasutage seda kiirklahvi |
|--------------------------------------|----------------------------|
| Filtrimine ettevõtte järgi                    | Alt+C                      |
| Filtrimine dimensiooni järgi                  | Alt+D                      |
| Välja Grupeerimisalus valimine            | Alt+G                      |
| Välistatud üksuste ja väärtuste kuvamine      | Alt+S                      |
| Tulemuste värskendamine                      | Alt+R                      |
| Valitud koosteüksuse välistamine  | Alt+X                      |
| Valitud readefinitsiooni välistamine  | Ctrl+B                     |
| Valitud dimensiooniväärtuse välistamine | Ctrl+D                     |
| Valitud aruande definitsiooni avamine  | Ctrl+R                     |
| Valitud readefinitsiooni avamine     | Ctrl+O                     |

 
<a name="see-also"></a>Vt ka
--------

[Finantsaruandlus](financial-reporting-intro.md)

[Aruande kujundaja liides](report-designer-interface.md)



