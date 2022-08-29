---
title: Müügitellimuse tarnekuupäevade arvutamine CTP-d kasutades
description: Lubamiseks võimekas (CTP) funktsioon võimaldab teil anda klientidele realistlikke kuupäevi, millal saate lubada kindlaid kaupu. See artikkel kirjeldab, kuidas seadistada ja kasutada CTP-d iga plaanimismootori jaoks (optimeerimine plaanimisel ja integreeritud mootoril).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 9a2d8a66fe7e68ebd5729a401af3f0efe04051b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229996"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Müügitellimuse tarnekuupäevade arvutamine CTP-d kasutades

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Lubamiseks võimekas (CTP) funktsioon võimaldab teil anda klientidele realistlikke kuupäevi, millal saate lubada kindlaid kaupu. Iga müügirea kohta saate sisestada kuupäeva, mis arvestab olemasolevat vaba kaubavaru, tootmisvõimsust ja transpordiaja.

CTP laiendab [lubamiseks saadaolevaid](../../sales-marketing/delivery-dates-available-promise-calculations.md) funktsioone, võttes arvesse võimsuse teavet. Kuigi ATP võtab arvesse ainult materjali saadavuse ja eeldab piiramatuid võimsuse ressursse, võtab CTP arvesse nii materjalide kui võimsuse kättesaadavust. Seega on sellel realistlikum pilt sellest, kas nõudlust saab antud aja jooksul rahuldada.

CTP töötab veidi teistmoodi, sõltuvalt kasutatavast koondplaneerimise mootorist (planeerimise optimeerimine või integreeritud mootor). See artikkel kirjeldab, kuidas seadistada see igale mootorile. Plaanimise optimeerimise CTP toetab praegu ainult alamkogumit CTP stsenaariumitest, mida integreeritud mootor toetab.

## <a name="turn-on-ctp-for-planning-optimization"></a>CtP plaanimise optimeerimise sisse lülitamine

Integreeritud koondplaneerimise mootori CTP on alati saadaval. Kuid kui soovite CTP-d kasutada optimeerimise planeerimiseks, peab see teie süsteemi jaoks sisse lülitatud olema. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Koondplaneerimine*
- **Funktsiooni nimi:** *(eelvaade) CTP optimeerimise planeerimiseks*

## <a name="how-ctp-compares-to-atp"></a>Kuidas CTP võrdleb ATP-ga

CTP ja ATP on sarnased, kuid CTP võib sageli anda täpsema tulemuse, nagu järgmine näide näitab.

Kaup A on kaup, mis koosneb kaupadest B ja C ning kauba A vaba kogus on 0 (null). Kui teete ATP kontrolli, mis võtab arvesse ainult materjale, on ATP kogus samuti 0 (null). Kuid KUI te teete CTP kontrolli, kontrollib süsteem kaupade B ja C kättesaadavust, kontrollige ressursse, mis on vajalikud nende kaubaks A teha ja arvutage, kui palju kaupa A teha saab. Lisaks saab CTP arvutamine kontrollida ressursse ja materjale, mida on vaja, et teha rohkem kaupu B ja C ning kasutada neid, et teha rohkem kaupa A.

CTP arvutus, mis võtab arvesse nii materjale kui ressursse, võib näidata suuremat kogust kui arvutus, mis kontrollib ainult materjale, eriti kui kontrollitav kaup on vastavalt tellimusele kokkupandav kaup. Teisisõnu põhineb CTP-funktsioon koosnevusarvutuse funktsioonil ja seda saab käitada valitud müügitellimuse rea puhul eeldatava tarnekuupäeva arvutamiseks.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Kuidas CTP erineb, sõltuvalt kasutatavast koondplaanimise mootorist

Järgmine tabel võtab kokku erinevused CTP ja plaanimise optimeerimise CTP vahel integreeritud koondplaneerimise mootori puhul.

| Element | Planeerimise optimeerimine | Integreeritud koondplaneerimise mootor |
|---|---|---|
| **Tarnekuupäeva kontrolli** säte tellimuste, tellimuse ridade ja toodete jaoks | *Planeerimise optimeerimise CTP* | *Ctp* |
| Arvutamise kellaaeg | Arvutuse käivitab plaanitud ülesandena dünaamilise plaani käitamine. | Arvutus käivitatakse müügitellimuse rea sisestamisel või uuendamisel kohe. |
| **CtP planeerimise optimeerimise oleku välja** väärtuse jaoks | <p>Tellimuste ja tellimuseridade *puhul, kus* dünaamilist plaani pole pärast tellimuste ja ridade loomist või viimast uuendamist käitatud, kuvatakse väärtus Pole valmis.</p><p>Tellimuste ja ridade *puhul*, kus CTP-d kasutati kinnitatud tarnekuupäevade arvutamiseks dünaamilist plaani käitades, kuvatakse valmis väärtus.</p> | Väärtus Valmis *kuvatakse* alati. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a> Tarnekuupäeva vaikekontrolli meetodite seada

Süsteem saab iga tellimuse- ja tellimuserea kohta tarnekuupäeva hinnangute arvutamiseks kasutada mitut meetodit. Seadistage tarnekuupäeva kontrollimeetod, mida soovite kasutada kõige sagedamini kui globaalset vaikemeetodit. Samuti saate igale tootele määrata individuaalsed avad. Hiljem saate vajaduse järgi alistada iga tellimuse ja/või tellimuserea vaikemeetodid.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a> Tarnekuupäeva globaalse vaikekontrolli seada

Tarnekuupäeva vaikekontrollimeetod rakendatakse kõigile uutele tellimuse ridadele, kus alistamine ei kehti. Ühe valimiseks järgige neid samme.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
1. **Valige vahekaardi Saadetised** kiirkaardil **·** **Tarne juhtimine väljal Tarnekuupäeva** kontroll meetod, mida soovite kasutada oma ettevõtte vaikemeetodina:

    - *Pole* – tarnekuupäevi ei arvutata.
    - *Müügi täitmisaeg* – müügi täitmisaeg on müügitellimuse koostamise ja kaupade lähetamise vaheline aeg. Tarnekuupäeva arvutamine põhineb vaikepäevade arvul ja ei arvesta lao kättesaadavust, teadaolevat nõudlust või plaanitud tarnet.
    - *ATP* – ATP on kauba kogus, mis on saadaval ja mida saab kliendile lubatud konkreetsel kuupäeval. ATP arvutamine sisaldab kehtestamata laosaldot, täitmisaegu, plaanitud sissetulekuid ja väljaminekuid.
    - *ATP + väljamineku* brutokasum – lähetuskuupäev võrdub ATP kuupäeva ja kauba väljaminekumarginaaliga. Väljamineku ohutusvaru on aeg, mis on vajalik kaupade saatmiseks ettevalmistamiseks.
    - *CTP – kasutage integreeritud koondplaneerimise mootori pakutavat CTP* arvutust. Kui kasutate planeerimise optimeerimist, *pole CTP* tarnekuupäeva kontrollmeetod lubatud ja kui see on valitud, põhjustab see arvutuse käitamisel vea.
    - *CTP plaanimise optimeerimise* jaoks – kasutage CTP arvutust, mille pakub planeerimise optimeerimine. See valik ei oma mingit mõju, kui kasutate integreeritud koondplaneerimise mootorit.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Tarnekuupäeva kontrolli alistamise seada üksikutele toodetele

Saate määrata alistamised kindlatele toodetele, kus soovite kasutada tarnekuupäeva kontrolli meetodit, mis pole see, mis on määratud teie globaalseks vaikemeetodiks.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toode, mida soovite seadistada.
1. Valige toimingupaani vahekaardil **Varude haldus** grupis **Tellimuse sätted** suvand **Tellimuse vaikesätted**.
1. **Seadke tellimuse vaikesätete** lehel müügitellimuse **kiirkaardil** **tarne juhtimise alistamise valikuks** *Jah*.
1. **Valige tarnekuupäeva kontrolli** väljal meetod, mida valitud toote puhul kasutada. Saadaval on samad valikud, mida kirjeldatakse jaotises [Globaalse tarnekuupäeva vaikekontroll](#global-default).

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a> CTP plaanimise optimeerimise arvutuste plaanimine

Kui kasutate CTP-d planeerimise optimeerimise jaoks, peate käivitama dünaamilise plaani, et käivitada süsteem CTP-arvutuste tegemiseks ja seejärel seadistama kinnitatud lähetus- ja vastuvõtukuupäevad kõigile asjakohastele tellimustele. Plaan peab sisaldama kõiki kaupu, mille jaoks on vaja lähetus- ja vastuvõtukuupäevi. (Kui kasutate CTP-d integreeritud plaanimismootori puhul, tehakse CTP arvutused kohalikult kohe. Seetõttu ei pea TE CTP tulemuste saavutamiseks käitama dünaamilist plaani.)

Et kuupäevad oleks kõigile kasutajatele õigeaegselt kättesaadavad, on soovitatav seadistada pakett-tööd, et käivitada vastavad plaanid korduvalt. Näiteks seadistatud dünaamilise plaani käivitamiseks iga 30 minuti järel seadistatakse kinnitatud lähetus- ja vastuvõtukuupäevad iga 30 minuti järel. Seega peavad kasutajad, kes sisestavad ja impordivad tellimusi, kinnitatud lähetus- ja vastuvõtukuupäevade saamiseks ootama kuni 30 minutit.

Dünaamilise plaani regulaarseks käitamiseks pakett-töö seadistamiseks järgige neid samme.

1. Koondplaneerimise **koondplaneerimise \> käivitamisel avage \> koondplaneerimine \>**.
1. **Seadke dialoogiboksi Koondplaneerimine** kiirkaardi **Parameetrid** väljale Koondplaan dünaamilisse plaani, **mida** soovite käitada.
1. Seadke kiirkaardiL **Käivita taustal** suvandi Pakktöötlus **väärtuseks** *Jah*.
1. Valige **kordumine** ja seadistage graafik vastavalt vajadusele.
1. **Graafiku salvestamiseks valige OK**.
1. Valige **OK**, et luua pakett-töö ja sulgege dialoogiboks.

## <a name="use-ctp-for-built-in-master-planning"></a>Kasuta integreeritud koondplaneerimiseks CTP-i

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Loo uus tellimus, kasutades integreeritud koondplaneerimise CTP-i

Iga kord kui lisate uue müügitellimuse või tellimuse rea, määrab süsteem sellele tarnekuupäeva vaikekontrolli meetodi. Tellimuse päis algab alati globaalse vaikemeetodiga. Kui tellitud kaubale on määratud alistamine, kasutab seda alistamist uus tellimuse rida. Vastasel juhul kasutab uus tellimuserida ka globaalset vaikemeetodit. Seepärast peaksite seadistama vaikemeetodid nii, et need ühtiksid tarnekuupäeva kontrolli meetodiga, mida kõige sagedamini kasutate. Tellimuse loomise järel saate tellimuse päise ja/või tellimuserea taseme vaikemeetodi vajaduse järgi alistada. Lisateabe saamiseks vt tarnekuupäeva [vaikekontrolli meetodite seadmist](#default-methods) ja olemasolevate [müügitellimuste muutmine CTP](#change-orders) kasutamiseks.

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Kinnitatud tarnekuupäevade kuva, kui kasutate integreeritud koondplaneerimiseks CTP-i

Kui kasutate integreeritud koondplaneerimise mootorit, rakendatakse CTP arvutused tellimustele ja/ **või tellimuse ridadele, kus tarnekuupäeva** kontrolli väli on seatud *CTP-le*.

Müügiridade puhul, mis kasutavad CTP-d valmis koondplaneerimiseks, **·** **seadistab** süsteem kinnitatud lähetuskuupäeva ja kinnitatud vastuvõtukuupäeva väljad automaatselt iga kord, kui salvestate müügirea. Kui teete hiljem vastavaid muudatusi müügireal (nt muutes selle kogust või laoaiti), arvutatakse kuupäevad kohe uuesti.

- Kinnitatud tarnekuupäevade vaatamiseks müügitellimuse real avage müügitellimus ja valige müügirida. Seejärel vaadake vahekaardil Tarne üle **rea üksikasjade kiirkaardil** väärtused **Kinnitatud** lähetuskuupäev ja **Kinnitatud** vastuvõtukuupäev **.**
- Terve tellimuse kinnitatud tarnekuupäevade vaatamiseks avage müügitellimus ja valige **päisevaade**. Seejärel vaadake kiirkaardil **Tarne** kiirkaart üle kinnitatud **lähetuskuupäeva ja** kinnitatud **vastuvõtukuupäeva** väärtused.

## <a name="use-ctp-for-planning-optimization"></a>Kasuta CTP-d optimeerimise planeerimiseks

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Loo uus tellimus, kasutades CTP-d optimeerimise planeerimiseks

Iga kord kui lisate uue müügitellimuse või tellimuse rea, määrab süsteem sellele tarnekuupäeva vaikekontrolli meetodi. Tellimuse päis algab alati globaalse vaikemeetodiga. Kui tellitud kaubale on määratud alistamine, kasutab seda alistamist uus tellimuse rida. Vastasel juhul kasutab uus tellimuserida ka globaalset vaikemeetodit. Seepärast peaksite seadistama vaikemeetodid nii, et need ühtiksid tarnekuupäeva kontrolli meetodiga, mida kõige sagedamini kasutate. Tellimuse loomise järel saate tellimuse päise ja/või tellimuserea taseme vaikemeetodi vajaduse järgi alistada. Lisateabe saamiseks vt tarnekuupäeva [vaikekontrolli meetodite seadmist](#default-methods) ja olemasolevate [müügitellimuste muutmine CTP](#change-orders) kasutamiseks.

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Kinnitatud tarnekuupäevade kuvamine CTP kasutamisel optimeerimise planeerimiseks

Kui kasutate planeerimise optimeerimist, rakendatakse CTP-arvutused tellimustele ja/või **·** *tellimuse ridadele, kus tarnekuupäeva kontrolli väli on seatud planeerimise optimeerimise JAOKS CTP-ks.*

Müügiridade puhul, mis kasutavad CTP-d planeerimise optimeerimiseks, **·** **on** väljad Kinnitatud lähetuskuupäev ja Kinnitatud vastuvõtukuupäev tühjad, kuni käivitate sobiva dünaamilise plaani (tavaliselt kasutades perioodilist pakett-tööd). Seejärel määratakse need automaatselt. Lisateavet vt ctP plaanimise [optimeerimise arvutustest](#batch-job).

Väli **CTP planeerimise optimeerimise oleku jaoks** näitab, kas igale reale, mis kasutab planeerimise optimeerimiseks CTP-d, on kinnitatud kuupäevad juba arvutatud. Väljal kuvatakse väärtus Pole *valmis ridade ja* tellimuste puhul, kus kinnitatud tarnekuupäevi pole veel arvutatud või need ei ole muude muudatuste tõttu enam kehtivad. See näitab arvutatud ridade *ja* tellimuste puhul väärtust Valmis. Saate vaadata iga rea ja kogu tellimuse olekut.

- Müügitellimuse rea oleku vaatamiseks avage müügitellimus ja valige müügirida. Seejärel vaadake vahekaardil **Tarne üle** rea üksikasjade kiirkaardil **optimeerimise** **oleku** ctP. Rea **kinnitatud lähetuskuupäeva** **ja** kinnitatud vastuvõtukuupäeva välju näidatakse samuti sellel vahekaardil pärast nende arvutamist.
- Terve tellimuse oleku vaatamiseks avage müügitellimus ja valige **päisevaade**. Seejärel vaadake tarne kiirkaardil **üle** **CTP optimeerimise oleku väärtuse** jaoks. Tellimuse **kinnitatud lähetuskuupäev** **ja** kinnitatud vastuvõtukuupäev kuvatakse samuti sellel vahekaardil pärast arvutamist.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Kui uuendate müügitellimuse rida pärast seda, kui plaanimise optimeerimise CTP on arvutanud selle kinnitatud kuupäevad, kustutab süsteem need kuupäevad kuni järgmise dünaamilise plaani käivitamisel.
> - Kui redigeerite seotud sätet, mis võib mõjutada olemasolevaid kinnitatud kuupäevi (nt muutes täitmiskuupäevi, reserveeringuid või märgistusi), peaksite kustutama kinnitatud kuupäevad vastavate olemasolevate tellimuste puhul. Selle toiminguga muudetakse iga vastava rea olekuks Pole *valmis*. See muudatus omakorda põhjustab süsteemi kinnitatud kuupäevade ümberarvutamise dünaamilist plaani käivitades.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a> Olemasolevate müügitellimuste muutmine CTP kasutamiseks

Tarnekuupäeva kontrolli väärtust **saate avatud** tellimuste jaoks igal ajal muuta. Väärtust saate muuta päise tasemel ja/või iga rea puhul vastavalt vajadusele.

### <a name="change-to-ctp-at-the-order-header-level"></a>CTP muutmine tellimuse päise tasemel

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Tellimuse muutmiseks nii, et see kasutaks CTP-d tellimuse päise tasemel, järgige neid samme.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused**.
1. Avage müügitellimus, mida soovite seadistada või looge uus.
1. Päiseteabe **avamiseks** müügitellimuse üksikasjade lehel **valige** päis.
1. **Seadke tarne** kiirkaardil **tarnekuupäeva kontrollväljale** üks järgmistest väärtustest, sõltuvalt kasutatavast plaanimismootorist:

    - *CTP – kasutage integreeritud koondplaneerimise mootori pakutavat CTP* arvutust. Kui kasutate planeerimise optimeerimist, pole *CTP* tarnekuupäeva kontrollmeetod lubatud. Kui valite selle väärtuse, ilmneb tõrge, kui arvutus käivitub.
    - *CTP plaanimise optimeerimise* jaoks – kasutage CTP arvutust, mille pakub planeerimise optimeerimine. See säte ei oma mingit mõju, kui kasutate integreeritud koondplaneerimise mootorit.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Muudatuse rakendamiseks valige **OK**.

### <a name="change-to-ctp-at-the-order-line-level"></a>CTPks muutmine tellimuse rea tasemel

Kui lõite tellimuserea erineva tarnekuupäeva kontrollmeetodiga, saate CTP-ks igal ajal muuta. Rea tasemel tehtud muudatused ei mõjuta muid ridu. Need võivad siiski põhjustada tellimuse üldine tarnekuupäevade edasi- või tagasini viimise, sõltuvalt sellest, kuidas iga uuendatud rea arvutus muutub. <!-- KFM: Confirm this intro at next revision -->

Tellimuse muutmiseks nii, et see kasutaks CTP-d integreeritud koondplaneerimiseks rea tasemel, järgige neid samme.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused**.
1. Avage müügitellimus, mida soovite seadistada või looge uus.
1. **Valige müügitellimuse rea** kiirkaardi **lehel** Müügitellimuse üksikasjad see müügitellimuse rida, mille soovite seadistada.
1. **·** **·** **Seadke** vahekaardi Tarne rea üksikasjade kiirkaardil tarnekuupäeva kontrollvälja väärtuseks üks järgmistest väärtustest, sõltuvalt kasutatavast plaanimismootorist:

    - *CTP – kasutage integreeritud koondplaneerimise mootori pakutavat CTP* arvutust. Kui kasutate planeerimise optimeerimist, pole *CTP* tarnekuupäeva kontrollmeetod lubatud. Kui valite selle väärtuse, ilmneb tõrge, kui arvutus käivitub.
    - *CTP plaanimise optimeerimise* jaoks – kasutage CTP arvutust, mille pakub planeerimise optimeerimine. See säte ei oma mingit mõju, kui kasutate integreeritud koondplaneerimise mootorit.

    Kuvatakse **saadaolevad lähetus- ja vastuvõtukuupäevad** ning kuvatakse saadaolevad lähetus- ja vastuvõtukuupäevad. Selles dialoogiboksis töötab tellimuseridade puhul sama hästi nagu tellimuse päise puhul (vt kirjeldust eelmisest jaotisest).

1. Valige toimingupaanil nupp **Salvesta**.
