---
title: Finantsaruannete loomine
description: See teema sisaldab finantsaruande koostamise üldteavet.
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e8b688cb1e4589eb076015d01dc4f0f0db14787e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688313"
---
# <a name="generate-financial-reports"></a>Finantsaruannete loomine

[!include [banner](../includes/banner.md)]

See teema sisaldab finantsaruande koostamise üldteavet.

Aruande loomiseks avage aruande definitsioon ja klõpsake seejärel tööriistaribal nuppu Loo. Avatakse aken Aruannete järjekorra olek ja näidatakse teie aruande asukohta järjekorras. Vaikimisi avaneb loodud aruanne veebivaaturis.

Aruannete loomiseks on saadaval järgmised suvandid.

- Graafiku seadistamine aruande või aruannete grupi automaatseks loomiseks
- Aruandest puuduvate kontode või andmete kontrollimine või aruande ja aruande täpsuse kinnitamine

Aruande loomisel kasutatakse valikuid, mille olete määranud valiku Aruande definitsioon vahekaartidel.

## <a name="generate-a-financial-report"></a>Finantsaruande loomine

Finantsaruande loomiseks minge jaotisse **Pearaamat** \> **Päringud ja aruanded** \> **Finantsaruanded**.

- Valige loodav aruanne ja klõpsake nuppu **Loo**.
- Täitke väli **Aruande kuupäev** ja klõpsake **OK**.

Kui aruanne on loodud, saab seda vaadata jaotises **Aruanded**.

Saate valida, kas soovite aruannet **Vaadata** või **Kustutada**.

Aruande loomiseks **Aruande koostaja** abil avage aruande definitsioon ja klõpsake seejärel tööriistaribal nuppu Loo. Avatakse aken Aruannete järjekorra olek ja näidatakse teie aruande asukohta järjekorras. Vaikimisi avaneb loodud aruanne veebivaaturis.

## <a name="schedule-report-generation"></a>Aruande loomise plaanimine
Paljudel ettevõtetel on aruannete põhikomplekt, mida kasutatakse plaanitud intervallidega, et äriprotsessidega vastavuses olla. Saate plaanida aruande regulaarselt loomise, näiteks iga päev, nädal, kuu või aasta. Tegemist võib olla ühe aruandega või mitut ettevõtet hõlmava aruannete rühmaga. Peate sisestama iga määratletud ettevõtte mandaadid, nagu aruandluspuu definitsiooniski. Kui mandaadid on kehtetud, kuvatakse aruandes ainult teave, millele teil on juurdepääsuõigus, nt ettevõte, kuhu olete sisse logitud. Väljundi teavet loetakse esmalt aruannete grupist ja seejärel üksikutest aruannetest.

Aruande graafikute loomisel ja salvestamisel kuvatakse need navigeerimispaanil suvandi Aruande graafikud all. Saate aruannete korraldamiseks kaustu luua. Kui üht graafikus olevat aruannet ei käitata, siis kõiki teisi aruandeid käitatakse endiselt.

> [!IMPORTANT]
> Graafikute loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll. Aruande käivitamisel kasutatakse aruande loomiseks graafiku loonud kasutaja mandaate.

### <a name="create-a-report-schedule"></a>Aruande graafiku loomine

1. Klõpsake aruande kujundaja menüüs Fail nuppu Uus ja seejärel valige Aruande graafik. Avaneb dialoogiboks Uus aruandegraafik.
2. Valige vahekaardilt Sätted plaanitav üksik aruanne või aruannete grupp. Saadaval on üksnes selle ettevõtte või koosteüksuse valiku aruanded või aruanderühmad, kuhu olete praegu sisse logitud.
3. Valige aruandegraafiku sisselülitamiseks märkeruut Aktiivne. Ainult aruande looja või administraator saavad aruandegraafiku aktiveerida või inaktiveerida.
4. Klõpsake ettevõtte mandaatide sisestamiseks nuppu Õigused. Vaikimisi kasutatakse teie selle ettevõtte sisselogimisteavet, kuhu olete sisse logitud. Kui näiteks aruandluspuu definitsioonid hõlmavad ka teisi ettevõtteid, valige suvand Kasuta eraldi mandaate ning sisestage seejärel mis tahes teise aruandegraafikus sisalduva ettevõtte mandaadid. Võite valida suvandi Windowsi autentimine või iga ettevõtte kasutajanime ja parooli tippida. Valige märkeruut Salvesta mandaadid nende ettevõtete mandaatide salvestamiseks ja seejärel klõpsake dialoogiboksi sulgemiseks nuppu OK.
5. Valige suvandi Sagedus väljalt Korduse käivitamine kuupäev, mil graafik käivitatakse. Vaikimisi valitakse klientarvuti praegune süsteemi kuupäev.
6. Valige väljal Aruande käitamine aruande käitamisaeg. Kui sisestate praegusest süsteemi ajast varasema aja, käitatakse aruannet järgmisel graafikus oleval kuupäeval.
7. Määratlege alal Kordumismuster aruande käitamissagedus. Vaikimisi valitakse Iga päev koos valiku Intervall (päevad) väärtusega 1. Muud valikud on Kord nädalas, Kord kuus ja Kord aastas.
8. Valige alal Kordumisvahemik aruande loomise lõpetamisaeg.

    - Lõppkuupäev puudub – aruandegraafikut käitatakse määramata ajani.
    - Määratud esinemiskordade arv – aruandegraafikut käitatakse määratud arv kordi ja inaktiveeritakse seejärel.
    - Lõppkuupäev – aruandegraafik lõpeb määratud kuupäeval.

9. Klõpsake tööriistaribal nuppu Salvesta. Sisestage dialoogiboksi Salvesta nimega aruande graafiku kordumatu nimi ja kirjeldus.

Aruande graafiku kopeerimiseks peab teil olema kujundaja või administraatori roll. Isegi kui administraator aruande graafikut muudab, säilitab aruanne aruande loonud kasutaja mandaate.

### <a name="copy-a-report-schedule"></a>Aruande graafiku kopeerimine

1. Klõpsake aruande kujundajas navigeerimispaanil suvandit Aruande graafikud ja avage kopeeritav aruande graafik.
2. Klõpsake menüüs Fail suvandit Salvesta nimega ning sisestage seejärel dialoogiboksi Save As graafiku uus nimi ja kirjeldus. Klõpsake OK ja navigeerimispaanil kuvatakse uus graafik.
3. Vajaduse korral muutke uues graafikus välju ja teavet ja seejärel klõpsake tööriistaribal nuppu Salvesta või klõpsake käsku Salvesta menüüs Fail.

Aruande graafiku kustutamiseks peate olema aruande graafiku omanik või teil peab olema administraatori roll.

### <a name="delete-a-report-schedule"></a>Aruande graafiku kustutamine

1. Klõpsake aruande kujundajas navigeerimispaanil suvandit Aruandegraafikud.
2. Valige kustutatav aruandegraafik ja klõpsake seejärel nuppu Kustuta või vajutage kustutusklahvi.
3. Kustutamise kinnituse dialoogiboksis klõpsake aruandegraafiku jäädavaks kustutamiseks nuppu Jah. Kui teil pole õigust graafikut kustutada, kuvatakse teade ja aruannet ei kustutata.

### <a name="credentials-and-report-schedules"></a>Mandaadid ja aruandegraafikud

Kui te ei sisesta kõikide aruandesse kaasatud ettevõtete puhul nõutavaid mandaate, kuvatakse aruande graafiku salvestamisel järgmine teade: „Peate sisestama mandaadid sellesse aruande graafikusse kaasatud ettevõtete puhul. Valige mandaatide sisestamiseks nupp Õigused.”

Näiteks logib kasutaja oma sisselogimisandmete ja parooliga Ettevõttesse A sisse. Kasutaja loob mitme ettevõtte andmete kogumiseks aruandluspuu definitsiooni kasutava aruande graafiku. Aruandegraafiku salvestamisel palutakse kasutajal sisestada teiste aruandluspuu definitsioonis määratud ettevõtete mandaadid. Mandaatide aegumisel ei looda aruande graafikus olevaid mõjutatud aruandeid kuni mandaatide värskendamiseni. Lubade värskendamise viitamiseks kuvatakse aruannete järjekorras teade. Aruande graafik nurjub mis tahes järgmiste asjaolude korral (kuna need nõuavad mandaate).

- Uus ettevõte on lisatud aruandluspuusse üksiku aruande puhul.
- Aruanderühmas olevat aruannet on muudetud.
- Aruanderühma on täiendava ettevõtte kohta uus aruanne lisatud.

Jätkamiseks klõpsake nuppu Load dialoogiboksis Aruande plaanimine ja seejärel sisestage sobivad mandaadid.

## <a name="missing-account-analysis-feature"></a>Puuduvate kontode analüüsi funktsioon
Saate otsida finantskontosid ja dimensioone, mis võivad olla puudu koosteüksuste grupi kõigis readefinitsioonides, aruandluspuu definitsioonides ja aruande definitsioonides. See on kasulik mitme konto või koosteüksuse loomisel või värskendamisel lühikese aja jooksul ja kui soovite kontrollida, kas kogu teave on aruannetesse kaasatud.

Puuduvad kontod määratakse, kasutades readefinitsiooni või aruandluspuu definitsiooni kõige madalamaid ja kõrgemaid väärtusi ja seejärel kuvatakse loend kontodest, mida pole readefinitsioonis või aruandluspuu definitsioonis, kuid on finantsandmetes. Kui puuduv konto on reamääratluse väärtustest suurem või väiksem, siis ei lisata kontot puuduvate kontode loendisse.

> [!TIP]
> Protsessi tuleb kinnitamiseks käitada enne igakuiste aruannete ja uute koosteüksuste loomist.

Väärtuste vahemikega aruannete puhul on kontode puudumine vähem tõenäoline. Võimaluse korral kasutage koosteüksuse vahemikke uute kontode lisamiseks nende loomisel. Kui aruande määratluses on määratud ettevõte @ANY, siis saate sisse logida kindlasse ettevõttesse ja käitada puuduvate kontode analüüsi.

> [!NOTE]
> Kui on lisatud uus ettevõte, peate lisama uue ettevõtte mis tahes olemasolevate aruannete aruandluspuudesse, vastasel korral ettevõtet puuduva konto analüüsi ei kaasata.

### <a name="run-missing-account-analysis"></a>Puuduva konto analüüsi käivitamine

1. Klõpsake aruande kujundajas suvandit Tööriistad ja seejärel klõpsake suvandit Puuduva konto analüüs.
2. Väljal Ettevõtte filter valige ettevõte, mille alusel tulemusi filtreerida, või valige Kõik (filter puudub), et kuvada kõikide saadaolevate ettevõtete tulemused.
3. Väljal Dimensiooni filter valige dimensioon, mille alusel tulemusi filtreerida, või valige Kõik (filter puudub), et kuvada kõikide saadaolevate dimensioonide teave.
4. Valige väljal Rühmitusalus suvand tulemuste sortimiseks. Võite sortida tulemusi asjakohase koosteüksuse alusel või dimensioonide ja väärtuste kogumite järgi.
5. Vaadake kuvatavad tulemused üle. Kui valite ülemisel paanil üksuse, kuvatakse alumisel paanil lisateavet erandi kohta. See hõlmab seotud dimensioone, väärtusi ja aruandeid.
6. Seotud üksuse avamiseks klõpsake loendi paanil kuvatavat seotud ikooni või paremklõpsake üksust ja valige käsk Ava. Mitme üksuse valimiseks hoidke alumisel paanil üksuste valimisel all klahvi Ctrl.
7. Mis tahes väärtuste, koosteüksuste või aruannete tagastamisel, mis ei tohiks aruandesse kaasatud olla, paremklõpsake üksust ja valige üksuse loendist eemaldamiseks käsk Välista või valige üksuse kõrval olev märkeruut Välista. Loendi värskendamisel välistatud üksusi ei kaasata. Alumisel paanil mitme üksuse valimiseks hoidke all klahvi Ctrl. Kõikide, sealhulgas varem analüüsist välistatud üksuste vaatamiseks valige märkeruut Kuva väljajäetud koosteüksused ja väärtused ning klõpsake käsku Värskenda.
8. Klõpsake käsku Värskenda, et värskendada erandeid, mida olete hallanud. Kõikide tulemuste värskendamiseks klõpsake valikut Jah, ainult hallatud üksuste värskendamiseks klõpsake valikut Ei.

    > [!NOTE]
    > Avamisel värskendatakse vormi automaatselt, v.a juhul kui vormi on avatud viimase 15 minuti jooksul.

9. Probleemide lahendamisel klõpsake dialoogiboksi sulgemiseks nuppu OK.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Kiirklahvid puuduva konto analüüsi puhul
Puuduva konto analüüsi käivitamisel on saadaval järgmised kiirklahvid.

| Toiming                           | Kasutage seda kiirklahvi |
|--------------------------------------|----------------------------|
| Filtrimine ettevõtte järgi                    | Alt+C                      |
| Filtreerimine dimensiooni järgi                  | Alt+D                      |
| Välja Rühmitamisalus valimine            | Alt+G                      |
| Väljajäetud koosteüksuste ja väärtuste kuvamine      | Alt+S                      |
| Tulemuste värskendamine                      | Alt+R                      |
| Valitud koosteüksuse välistamine  | Alt+X                      |
| Valitud reamääratluse välistamine  | Ctrl+B                     |
| Valitud dimensiooniväärtuse välistamine | Ctrl+D                     |
| Valitud aruandemääratluse avamine  | Ctrl+R                     |
| Valitud reamääratluse avamine     | Ctrl+O                     |


## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)

[Aruandekoosturi liides](report-designer-interface.md)
