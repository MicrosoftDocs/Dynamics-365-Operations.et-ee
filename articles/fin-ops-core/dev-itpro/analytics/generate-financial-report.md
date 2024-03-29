---
title: Finantsaruannete loomine
description: See artikkel annab teavet finantsaruande loomise kohta.
author: jinniew
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2f55fe1a23735d8631a5918fa49e08f74eee4d37
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802765"
---
# <a name="generate-financial-reports"></a>Finantsaruannete loomine

[!include [banner](../includes/banner.md)]

See artikkel annab teavet finantsaruande loomise kohta.

Aruande loomiseks avage aruande definitsioon ja valige tööriistaribal käsk **Loo**. Avab **aruande järjekorra** olekulehe ja näitab teie aruande asukohta järjekorras.

Aruande loomise edenedes võivad järgmised aruandejärjekorra olekunäidikud olla aruandejärjekorra **oleku lehel nähtavad** .

| Olek          | Osariik | Kirjeldus|
|-----------------|--------|--------------------|
| Järjekorda lisamine        | Ajutised |Aruande definitsioon kinnitatakse enne aruande asetamist loomise järjekorda.                    |
| Järjekorras          | Ajutised | Aruanne sisestab aruande loomise järjekorra ja ootab töötlemist.                      |
| Töötlemisel      | Ajutised | See olek järgib tavaliselt olekut **Järjekorras** ning viib tavaliselt **töötlemise lõpetamisel** lõplikule olekule üle.       |
| Järeltöötlemisel | Ajutised | See olek järgib töötlemise **olekut** ja näitab, et kogutakse kõik aruande andmed, kuid teostatakse sellised tegevused nagu kalkulatsioon ja ümberarvestus.            |
| Tühistamine      | Ajutised | Aruandlus tühistatakse kasutaja nõudmisel. See olek tuleneb kasutaja taotletud tühistamisest aruandele olekus Järjekorras **või**  **Töötlemine** . Süsteem püüab panna aruande Tühistatud **olekusse**, välja arvatud juhul, kui süsteem on liiga kaugele jõudnud ja peab selle teises olekus lõpetama. |
| Tühistatud        | Lõplik | Aruanne on töötlemise lõpetanud, kuid seda ei lõpetatud kasutaja nõutud peatamise tõttu.            |
| Lõpule viidud       | Lõplik | Aruanne on kasutamiseks valmis.                      |
| Nurjus          | Lõplik | Aruanne lõpetas töötlemise, kuid ebaõnnestus ja seda ei tohi kasutada. |

Vaikimisi avaneb loodud aruanne veebivaaturis. Aruannete loomiseks on saadaval järgmised suvandid.

- Graafiku seadistamine aruande või aruannete grupi automaatseks loomiseks
- Aruandest puuduvate kontode või andmete kontrollimine või aruande ja aruande täpsuse kinnitamine

Aruande loomisel kasutatakse suvandeid, mis te olete määranud aruande definitsiooni vahekaartidele.

## <a name="generate-a-financial-report"></a>Finantsaruande loomine

Finantsaruande loomiseks minge jaotisse **Pearaamat** \> **Päringud ja aruanded** \> **Finantsaruanded**.

- Valige loodav aruanne ja klõpsake nuppu **Loo**.
- Täitke väli **Aruande kuupäev** ja klõpsake **OK**.

Kui aruanne on loodud, saab seda vaadata jaotises **Aruanded**.

Saate valida, kas soovite aruannet **Vaadata** või **Kustutada**.

Aruande loomiseks **Aruande koostaja** abil avage aruande definitsioon ja klõpsake seejärel tööriistaribal **Loo** nuppu. Avab **aruande** järjekorra olekulehe ja näitab teie aruande asukohta järjekorras. Vaikimisi avaneb loodud aruanne veebivaaturis.

## <a name="report-groups"></a>Aruanderühmad

Aruandegrupid on tõhus viis luua korraga mitu aruannet. Oletame näiteks, et te teate, et kuu lõpus loovad teie kasutajad kaheksa aruannet igas kuus. Looge aruandegrupp ja selle asemel et valida grupis kõigi kaheksast aruandest **Loomine** võite valida aruandegrupi jaoks väärtuse **Loo** ja kaheksa aruannet luuakse ühes etapis. Kui valitud aruandegrupi aruanded on loodud, **·**  saate üksikute aruannete vaatamiseks minna finantsaruannetesse (**Pearaamat > Aruanded ja aruanded >** Finantsaruanded). Lõpetage järgmised etapid tingimusliku näidisaruande seadistamiseks.

1. Valige **aruandekujundajas** aruandegrupid **·**. 
2. Valige olemasolevad aruande definitsioonid, mida oma aruandegruppi kaasata. 
3. Valige alistav ettevõte, üksikasjad ja kuupäeva sätted igast gruppi kaasatud aruandest.
   Soovitame seadistada **Ettevõtte** **Periood** **Aasta** ja **Üksikasjaliku taseme** iga aruande jaoks. 
4. Salvestage aruande grupp.

## <a name="schedule-report-generation"></a>Aruande loomise plaanimine
Paljudel ettevõtetel on aruannete põhikomplekt, mida kasutatakse plaanitud intervallidega, et äriprotsessidega vastavuses olla. Saate plaanida aruande regulaarselt loomise, näiteks iga päev, nädal, kuu või aasta. Tegemist võib olla ühe aruandega või mitut ettevõtet hõlmava aruannete rühmaga. Peate sisestama iga määratletud ettevõtte mandaadid, nagu aruandluspuu definitsiooniski. Kui mandaadid ei kehti, kuvab aruanne ainult teabe, mille juurde teil on juurdepääs, nt ettevõte, mille olete praegu sisse loginud. Väljundi teavet loetakse esmalt aruannete grupist ja seejärel üksikutest aruannetest.

Aruandegraafikute loomisel ja salvestamisel kuvatakse need navigeerimispaanil aruandegraafikute **all**. Saate aruannete korraldamiseks kaustu luua. Kui üht graafikus olevat aruannet ei käitata, siis kõiki teisi aruandeid käitatakse endiselt.

> [!IMPORTANT]
> Graafikute loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll. Aruande käivitamisel kasutatakse aruande loomiseks graafiku loonud kasutaja mandaate.

### <a name="create-a-report-schedule"></a>Aruande graafiku loomine

1. Valige aruandekujundaja menüüs Fail suvand Uus **ja** seejärel **aruandegraafik** . **·** **·** Avaneb **uue aruandegraafiku** dialoogiboks.
2. Valige vahekaardilt **Sätted**, plaanitav üksik aruanne või aruannete grupp. Saadaval on üksnes selle ettevõtte või koosteüksuse valiku aruanded või aruanderühmad, kuhu olete praegu sisse logitud.
3. Aruande graafiku sisselülitamiseks valige märkeruut **Aktiivne**. Ainult aruande looja või administraator saavad aruandegraafiku aktiveerida või inaktiveerida.
4. Ettevõtte mandaatide sisestamiseks klõpsake nuppu **Load**. Vaikimisi kasutatakse teie selle ettevõtte sisselogimisteavet, kuhu olete sisse logitud. Kui kaasatud on muud ettevõtted, näiteks aruandluspuu definitsioonides, valige suvand **Kasuta eraldi mandaate** ja seejärel sisestage mandaadid muu aruande graafikusse kaasatud ettevõtte puhul. Saate valida Windowsi **autentimise** või tippida iga ettevõtte kasutajanime ja parooli. Valige märkeruut **Salvesta mandaadid** nende ettevõtete mandaatide salvestamiseks ja seejärel klõpsake dialoogiboksi sulgemiseks nuppu **OK**.
5. Valige suvandi **Sagedus** väljalt **Korduse käivitamine** kuupäev, millal graafik käivitatakse. Vaikimisi valitakse klientarvuti praegune süsteemi kuupäev.
6. Valige väljalt **Käivita aruanne** aeg, mil aruanne tuleks käivitada. Kui sisestate praegusest süsteemi ajast varasema aja, käitatakse aruannet järgmisel graafikus oleval kuupäeval.
7. Määrake alal **Kordumismuster**, kui tihti aruanne käivitada. Vaikimisi valitakse väärtus **Igapäevane** väärtusega **Intervalli (päevad)**  väärtusega **1**. Muude valikute hulka kuuluvad kord **nädalas,** **kord kuus** ja kord aastas **.**
8. Valige alas **Kordumisvahemik**, millal tuleks aruande loomine lõpetada.

    - **Lõppkuupäev puudub** – aruande graafikut käivitatakse määramata aja jooksul.
    - **Määratud esinemiste arv** – aruande graafikut käivitatakse määratud arvu kordi ja seejärel inaktiveeritakse.
    - **Lõpeta** – aruande graafik lõpeb määratud kuupäeval.

9. Valige käsk **Salvesta**. Dialoogiboksis Salvesta **nimega** sisestage aruandegraafiku kordumatu nimi ja kirjeldus.

Aruande graafiku kopeerimiseks peab teil olema kujundaja või administraatori roll. Isegi kui administraator aruande graafikut muudab, säilitab aruanne aruande loonud kasutaja mandaate.

### <a name="copy-a-report-schedule"></a>Aruande graafiku kopeerimine

1. Aruandekujundajas valige **navigeerimispaanil** Aruandegraafikud ja avage kopeerimiseks aruandegraafik.
2. Valige menüü **Fail** käsk Salvesta **nimega** ja sisestage graafikule dialoogiboksis Salvesta nimega uus nimi **ja** kirjeldus. Klõpsake nuppu **OK** ja navigeerimispaanil kuvatakse uus graafik.
3. Vajaduse korral muutke uues graafikus välju ja teavet ning seejärel klõpsake tööriistaribal nuppu **Salvesta** või klõpsake käsku **Salvesta** menüüs **Fail**.

Aruande graafiku kustutamiseks peate olema aruande graafiku omanik või teil peab olema administraatori roll.

### <a name="delete-a-report-schedule"></a>Aruande graafiku kustutamine

1. Aruandekujundajas valige **navigeerimispaanil** Aruandegraafikud.
2. Valige kustutatav aruande graafik ja seejärel klõpsake suvandit **Kustuta** või vajutage klahvi **Kustuta**.
3. Klõpsake kustutamise kinnitamise dialoogiboksis suvandit **Jah** aruande graafiku jäädavaks kustutamiseks. Kui teil pole graafiku kustutamise õigust, kuvatakse teade ja aruannet ei kustutata.

### <a name="credentials-and-report-schedules"></a>Mandaadid ja aruandegraafikud

Kui te ei sisesta mandaate, mis on nõutud kõigis aruannetes kaasatud ettevõtetes, saate aruande ajakava salvestamisel järgmise teate: "Peate sisestama oma mandaadid ettevõtetele, mis sisalduvad selles aruande ajakavas. Valige oma **mandaatide** sisestamiseks nupp Õigused."

Näiteks logib kasutaja oma sisselogimisandmete ja parooliga Ettevõttesse A sisse. Kasutaja loob mitme ettevõtte andmete kogumiseks aruandluspuu definitsiooni kasutava aruande graafiku. Aruandegraafiku salvestamisel palutakse kasutajal sisestada teiste aruandluspuu definitsioonis määratud ettevõtete mandaadid. Kui teie mandaadid aeguvad, ei looda aruandegraafikus mõjutatud aruandeid enne, kui mandaadid on värskendatud. Lubade värskendamise viitamiseks kuvatakse aruannete järjekorras teade. Aruande graafik nurjub mis tahes järgmiste asjaolude korral (kuna need nõuavad mandaate).

- Uus ettevõte on lisatud aruandluspuusse üksiku aruande puhul.
- Aruanderühmas olevat aruannet on muudetud.
- Aruanderühma on täiendava ettevõtte kohta uus aruanne lisatud.

Jätkamiseks valige dialoogiboksis **Aruande** plaanimine nupp **Õigused** ja sisestage seejärel sobivad mandaadid.

## <a name="missing-account-analysis-feature"></a>Puuduvate kontode analüüsi funktsioon
Saate otsida finantskontosid ja dimensioone, mis võivad olla puudu koosteüksuste grupi kõigis readefinitsioonides, aruandluspuu definitsioonides ja aruande definitsioonides. See on kasulik mitme konto või koosteüksuse loomisel või värskendamisel lühikese aja jooksul ja kui soovite kontrollida, kas kogu teave on aruannetesse kaasatud.

Puuduvad kontod määratletakse readefinitsiooni või aruandluspuu definitsiooni madalaima ja kõrgeima väärtusega ning seejärel kuvatakse nende kontode loend, mis ei ole readefinitsioonis või aruandluspuu definitsioonis, kuid mis on finantsandmetes. Kui puuduv konto on suurem või väiksem kui readefinitsiooni väärtused, ei kaasata seda kontot puuduvate kontode loendisse.

> [!TIP]
> Protsessi tuleb kinnitamiseks käitada enne igakuiste aruannete ja uute koosteüksuste loomist.

Väärtuste vahemikega aruannete puhul on kontode puudumine vähem tõenäoline. Võimaluse korral kasutage koosteüksuse vahemikes uusi kontosid nende loomisel. Kui aruande määratluses on määratud ettevõte @ANY, siis saate sisse logida kindlasse ettevõttesse ja käitada puuduvate kontode analüüsi.

> [!NOTE]
> Kui on lisatud uus ettevõte, peate lisama uue ettevõtte mis tahes olemasolevate aruannete aruandluspuudesse, vastasel korral ettevõtet puuduva konto analüüsi ei kaasata.

### <a name="run-missing-account-analysis"></a>Puuduva konto analüüsi käivitamine

1. Valige aruandekujundajas suvand **Tööriistad** ja seejärel puuduv **kontoanalüüs**.
2. Valige väljalt **Ettevõtte filter** ettevõte, mille põhjal tulemusi filtreerida või valige suvand **Kõik (filter puudub)** tulemuste kuvamiseks kõigilt saadaolevatelt ettevõtetelt.
3. Valige väljalt **Dimensioonifilter** dimensioon, mille põhjal tulemusi filtrida või valige suvand **Kõik (filter puudub)** dimensiooniteabe kuvamiseks kõigi saadaolevate dimensioonide puhul.
4. Valige väljalt **Grupeerimisalus** tulemuste sortimiseks suvand. Võite sortida tulemusi asjakohase koosteüksuse alusel või dimensioonide ja väärtuste kogumite järgi.
5. Vaadake kuvatavad tulemused üle. Kui valite ülemisel paanil üksuse, kuvatakse alumisel paanil lisateavet erandi kohta. See hõlmab seotud dimensioone, väärtusi ja aruandeid.
6. Seotud üksuse avamiseks klõpsake loendi paanil kuvatavat seotud ikooni või paremklõpsake üksust ja valige käsk **Ava**. Mitme üksuse valimiseks hoidke alumisel paanil all klahvi **Ctrl** mitme üksuse valimiseks.
7. Kui tagastatakse mis tahes väärtused, ehitusplokkid või aruanded, mida ei peaks analüüsi kaasama, **paremklõpsake** kaupa ja valige suvand Välista või märkige kauba kõrval ruut Välista, **et** eemaldada kaup loendist. Loendi värskendamisel ei kaasata välja jäetud kaupu. Mitme üksuse valimiseks hoidke alumisel paanil all klahvi **Ctrl** mitme üksuse valimiseks. Kõikide üksuste (sh kõigi **eelnevalt analüüsist väljajäetavate tulemuste) vaatamiseks märkige ruut Kuva** välistatud koosteüksused ja väärtused ning valige **suvand Värskenda**.
8. Valige **suvand** Värskenda, et värskendada erandeid, mille olete läbinud. Kõigi tulemuste täielikuks värskendamiseks klõpsake suvandit **Jah** või klõpsake osutatud üksuste osaliseks värskendamiseks suvandit **Ei**.

    > [!NOTE]
    > Kui lehekülg pole viimase 15 minuti jooksul avatud, uuendatakse vormi avamisel automaatselt.

9. Probleemide lahendamisel klõpsake dialoogiboksi sulgemiseks nuppu **OK**.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Kiirklahvid puuduva konto analüüsi puhul
Puuduva konto analüüsi käivitamisel on saadaval järgmised kiirklahvid.

| Toiming                           | Vajutage nuppu  |
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
