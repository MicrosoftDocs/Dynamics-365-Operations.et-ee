---
title: Tarnegraafik
description: Selles teemas kirjeldatakse tarnete ajakava lehte ja selle võimalusi.
author: ChristianRytt
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d2f0f38d86ae307ef80bd02901e19a08d5e30ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578364"
---
# <a name="supply-schedule"></a>Tarnegraafik

[!include [banner](../includes/banner.md)]

**Tarnete ajakava** leht näitab põhjalikku ülevaadet toote või tootepere pakkumisest ja nõudlusest. Teavet filtreeritakse asukoha, üldplaani ja perioodide järgi. Lehte saate kasutada ka uute tellimuste loomiseks, olemasolevate kavandatud tellimuste muutmiseks ja üldplaneerimise käivitamiseks.

## <a name="open-the-supply-schedule-page"></a>Tarnete ajakava lehe avamine

Saate avada **Tarnete ajakava** lehe järgmistel viisidel:

- Avage **Koondplaneerimine \> Koondplaneerimine \> Tarnete ajakava**. Dialoogiboksis **Muuda filtrit** määrake plaan ja toode, mida otsite, sisestades filtriväärtused pakutavatele väljadele. (Selle teema ülejäänud osas nimetatakse teie sisestatud filtriväärtuste kogumit "filter" või "praegune filter".) Kui olete lõpetanud, valige **OK**.
- Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**. Valige või avage toode. Seejärel tehke tegumirea vahekaardil **Plaan** grupis **Vaade** valik **Tarnete ajakava**.
- Avage **Koondplaneerimine \> Seadistus \> Nõudluse prognoos \> Kauba jaotamise võtmed**. Valige kauba eraldamisvõti, mida kasutatakse tooteperena. Valige toimingupaanil **Tarnete ajakava**.
- Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**. Valige või avage plaanitud tellimus. Seejärel tehke tegumirea vahekaardil **Vaade** grupis **Vaade** valik **Tarnete ajakava**.

> [!NOTE]
> Kui avate toote, tootepere või kavandatud tellimuse lehe **Tarnete ajakava**, ei pea te filtriväärtusi sisestama. Süsteem kasutab perioodi vaikemall.

## <a name="use-the-supply-schedule-page"></a>Tarnete ajakava lehe kasutamine

**Tarnete ajakava** leht koosneb ülemisest osast, **Perioodi lõpu inventuur** Kiirkaardist, mis on täiendav kiirkaart, mis muutub nähtavaks ülemises jaotises valitud rea põhjal, ja FactBoxi paanil. (FactBoxi paani avamiseks ja FactBoxi vaatamiseks valige lehe paremas servas **Seotud teave**.)

### <a name="upper-section"></a>Ülemine jaotis

Lehe **Tarnete ajakava** ülemises osas on ruudustik, mis näitab järgmisi toote või tootepere andmeid. Need andmed on jaotatud perioodide järgi, mis on määratletud filtri väärtusega **Perioodimall**.

- **Perioodi algusinventuur** – See rida näitab eeldatavat varude saldot perioodi alguses, kui süsteemis esitatakse kõik tellimused.
- **Perioodi lõpuinventuur** – See rida näitab eeldatavat varude saldot perioodi lõpus, kui süsteemis esitatakse kõik tellimused.
- **Perioodi lõpu seotud varud** – see rida näitab varude hulka perioodi lõpus, mis on seotud tulevase nõudlusega.
- **Perioodi netotarne** – See rida näitab perioodi pakkumise ja nõudluse erinevust.
- **Minimaalne laoseis** – See sõlm näitab toote või tootepere turvavarusid. Selle sõlme laiendamiseks või ahendamiseks valige see ja seejärel valige tööriistareal **Laienda** või **Ahenda**. Seda sõlme näidatakse ainult siis, kui toote või tootepere jaoks on olemas varu.
- **Nõudlus** – See sõlm näitab toote või tootepere nõudlust. Nõudlus on rühmitatud tehinguliigi järgi. Selle sõlme laiendamiseks või ahendamiseks valige see ja seejärel valige tööriistareal **Laienda** või **Ahenda**. Nõudmistehingute tüübid hõlmavad müüki, ülekandeid ja varude töölehti. Seda sõlme näidatakse ainult siis, kui toote või tootepere jaoks on olemas nõudlus.
- **Tarne** – See sõlm näitab toote või tootepere tarnet. Tarne on rühmitatud tehinguliigi järgi. Selle sõlme laiendamiseks või ahendamiseks valige see ja seejärel valige tööriistareal **Laienda** või **Ahenda**. Tarnetehingute tüübid hõlmavad tootmist, ostmist ja üleandmist. Seda sõlme näidatakse ainult siis, kui toote või tootepere jaoks on olemas tarne.

Paljud saadaolevad tööriistarea nupud, FactBoxi kuvad ja FastTab ekraanid sõltuvad ülemises jaotises tehtud valikutest. Tavaliselt valite tehingutüübi, valides ühe rea **Tarne** või **Nõudlus** sõlme alt. Seejärel valite perioodi, valides valitud rea jaoks konkreetse veeru.

Tööriistariba ruudustiku kohal lehe **Tarnete ajakava** ülemises osas on järgmised nupud:

- **Laienda/Ahenda** – Laiendage või ahendage valitud sõlme, näiteks **Nõudlus** sõlme, **Tarne** sõlme ja nende alamsõlmi. (Sõlmed näitavad **\[+\]** või **\[-\]** eesliidet, mis näitab, kas need on praegu ahendatud või laiendatud.)
- **Uus** – menüü avamine, kus iga käsk avab omakorda dialoogiboksi või lehe, mis võimaldab valiku jaoks lisada teatud tüüpi üksuse. Saadaolevate käskude hulka kuuluvad **Pakkumise prognoos**, **Kavandatud tellimus**, **Ajastatud kanban**, **Uus tootmistellimus**, **Ostu tellimus** ja **Ülekande tellimus**.
- **Üldplaneerimine** – Käivitage üldplaneering. Ilmub dialoogiboks, kus saate määrata käivitatava plaani. Vaikimisi on väli **Üldplaan** kehtivale filtrile vastav.
- **Max. aruanne lõpetatuna** – avage **Max. aruanne lõpetatuna** leht praeguses filtris määratletud toote kohta.
- **Kavandatud tellimuste värskendamine** – avage leht **Planitud tellimused**, mis näitab praeguses filtris määratletud toote või tootepere jaoks kavandatud tellimusi.
- **Tasand** – Levitage planeeritud tellimusi vastavalt kuvatava dialoogiboksi seadetele.
- **Materjaliplaani poliitika asukoha järgi** – Avage praeguses filtris määratletud toote leht **Kauba katvus**.
- **Kanbani reegel** – Avage praeguses filtris määratletud toote **Kanbani reeglid** leht.

### <a name="fasttabs"></a>Kiirkaardid

**Tarnete ajakava** leht võib sisaldada järgmisi kiirkaarte:

- **Perioodi lõpu varud** – Sellel kiirkaardil kuvatakse ajavahemiku lõpu varude andmed graafilises vormingus.
- **Tarneprofiil** – Sellel kiirkaardil kuvatakse tarne andmed graafilises vormingus. See muutub nähtavaks, kui valite **Tarne** sõlme või ülemises osas selle all oleva joone.
- **Kokkuvõte** – Sellel kiirkaardil kuvatakse kokkuvõtlikud üksikasjad, mis on seotud ülemises jaotises valitud tehingutüübiga. Näiteks kui valite sõlme **Nõudlus** alt **Müük**, kuvab see kiirkaart väljad, mis on seotud müügitellimustega, näiteks **Soovitud müügitellimuste read** või **Kogusumma**. Kui valite **Tootmistellimused** sõlme **Tarne** alamsõlme **Tootmine** alt, kuvatakse sellel kiirkaardil väljad, mis on seotud tootmistellimustega, näiteks **Tootmistellimused ajastatud** või **Kokku planeeritud**. Välja väärtused sõltuvad ülemises jaotises valitud perioodist. 
- **\[Tehingutüüp\] - \[Periood\]** – Sellel kiirkaardil kuvatakse ülemises jaotises valitud tehingutüübi ja -perioodi tellimused. Kiirkaardi nimi kajastab neid valikuid. Näiteks võib selle nimi olla **Müügitellimused - mahajäämus** või **Tootmistellimused - nädal 37**.

### <a name="action-pane"></a>Toimingupaan

Tegumireal on saadaval järgmised nupud:

- **Muuda filtrit** - Avage dialoogiboks **Muuda filtrit**, kus saate filtri väärtusi värskendada ja seejärel uuesti avada lehe **Tarnete ajakava**, mis kajastab värskendatud filtrisätteid.
- **Näita viivitusi** – Tõstke ülemises jaotises esile asjakohased read, kui seda tüüpi tehingu korral on viivitus.

### <a name="factbox-pane"></a>FactBoxi paan

FactBoxi paani avamiseks ja FactBoxi vaatamiseks valige lehe paremas servas **Seotud teave**. **Tarnete ajakava** lehel on saadaval järgmised FactBoxid:

- **Kauba üksikasjad** – See FactBox näitab põhiteavet toote kohta, mis on määratletud praeguses filtris. See on tühi, kui määrasite tootepere filtris.
- **Toimingud** – See FactBox näitab ülemises jaotises valitud tehingutüübi tellimuste toiminguid.
- **Viivitused** – See FactBox näitab ülemises jaotises valitud tehingutüübi tellimuste viivitsued.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
