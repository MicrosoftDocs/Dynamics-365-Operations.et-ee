---
title: Kindlad plaanitud tellimused
description: See teema kirjeldab, kuidas kinnitada planeeritud tellimusi. Kui planeeritud tellimused on kinnitatud, teisendatakse need tegelikeks ostutellimusteks, ülekandekorraldusteks või tootmistellimuseks.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a4f882f1abc9f758aca77b137b28aa973f925ea9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019490"
---
# <a name="firm-planned-orders"></a>Kindlad plaanitud tellimused

[!include [banner](../../includes/banner.md)]

Planeeritud tellimused tuleb üldplaneerimise protsessi osana *kinnitada* (st vabastada). Kui planeeritud tellimused on kinnitatud, teisendatakse need tegelikeks ostutellimusteks, ülekandekorraldusteks või tootmistellimuseks. Need on tuntud ka kui *väljastatud tellimused* või *avatud tellimused*.

Planeeritud tellimuste kinnitamiseks on kolm meetodit:

- **Käsitsi kinnitamine** – valige loendist planeeritud tellimused ja käivitage protsess käsitsi.
- **Automaatne kinnitamine** – määratlege laovarude gruppide, üksikute kaupade ning kaupade ja üldplaanide kombinatsioonide vaike-kinnitamise ajapiir. Seejärel määratakse plaanitud tellimused üldplaneerimise käitamise ajal automaatselt, kui tellimuse kuupäev jääb kinnitamiseks määratud ajapiiri piiresse.
- **Päringupõhine kinnitamine** – saate määratleda atribuutide põhjal päringu planeeritud tellimuste valimiseks. Saate seadistada päringu käivitamiseks pakett-töö ja regulaarsel graafikul kindlad tellimused.

Selles teemas kirjeldatakse üksikasjalikult iga meetodit.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Luba selles teemas kirjeldatud funktsioonid

Enamik planeeritud tellimuse funktsioone on saadaval Microsoft Dynamics 365 Supply Chain Management standardinstallide puhul, mis kasutavad planeerimise optimeerimist. Kuid mõned selles teemas kirjeldatud funktsioonid tuleb funktsioonihalduses enne nende kasutamist sisse lülitada.

### <a name="enable-parallelized-firming-of-planned-orders"></a>Planeeritud tellimuste paralleelkinnitamine

Paralleelne kinnitamine aitab kinnitamisprotsessi kiirendada, seda mitme lõime vahel paralleelselt. Selline lähenemine võib olla kasulik, kui paljud planeeritud tellimused on kinnitatud.

Et teha see funktsioon süsteemis kättesaadavaks, minge [Funktsioonihaldus](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ja lülitage sisse *planeeritud tellimuste paralleelse kinnitamise* funktsioon.

### <a name="enable-planned-order-firming-with-filtering"></a>Lubage planeeritud tellimuse kinnitamine filtreerimisel

Planeeritud tellimuste kinnitamine filtreerimisel võimaldab määratleda loogilised kriteeriumid, et valida, milliseid planeeritud tellimusi kinnitada. Saate ka eelversiooni vaadata, millised plaanitud tellimused valiti, protsessi taustal käitada ja/või planeerida seda pakett-tööna.

Et teha see funktsioon süsteemis kättesaadavaks, minge [Funktsioonihaldus](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ja lülitage sisse *Planeeritud tellimuste paralleelse kinnitamise* funktsioon.

### <a name="enable-auto-firming-for-planning-optimization"></a>Lubage automaatne kinnitamine planeerimise optimeerimise käigus

Automaatkinnitamine võimaldab teil kinnitada planeeritud tellimused koondplaneerimise protsessi osana kinnitamise ajaaknas. Supply Chain Management integreeritud planeerimismootori puhul toetatakse alati automaatset kinnitamist. Kuid selleks, et seda kasutada ka planeerimise optimeerimisel, peate selle funktsiooni sisse lülitama.

Et teha see funktsioon süsteemis kättesaadavaks, minge [Funktsioonihaldus](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ja lülitage sisse *Planeeritud tellimuste paralleelse kinnitamise* funktsioon.

## <a name="manually-firm-planned-orders"></a>Planeeritud tellimuste käsitsi kinnitamine

Planeeritud tellimuste käsitsi kinnitamiseks otsige ja valige planeeritud tellimused, mida soovite kinnitada ning seejärel käivitage kinnitamisprotsess käsitsi.

1. [Kõigi planeeritud tellimuste loendilehe](approved-planned-order.md#view-planned-orders)avamine.
1. Loendi filtreerimiseks ja sortimiseks kasutage välja **Filter**, **Plaan** ja veerupäiseid, et leida otsitav planeeritud tellimus.
1. Märkige ruut iga planeeritud tellimuse puhul, mille soovite kinnitada. Kui soovite kõikide praegu leheküljel loetletud planeeritud tellimuste kinnitamist (filtrite alusel), jätke see etapp vahele.
1. Klõpsake tegumiribal ühte järgmistest valikutest:

    - **Kinnita** – Kinnitage ainult valitud planeeritud tellimused.
    - **Kinnita kõik** – Kinnitage kõik praegu leheküljel loetletud plaanitud tellimused (filtrite alusel), sõltumata valitud märkeruutudest. See suvand võib olla kasulik juhul, kui kinnitate suure hulga planeeritud tellimusi.

1. Seadke dialoogiboksis **Kinnitamine** kiirkaardil **Parameetrid** järgmised väljad. (Paljud neist väljadest saavad vaikeväärtused vahekaardilt **Standardne uuendamine** lehel **Üldplaneerimise parameetrid**.)

    - **Uuenduste märkimine** – Valige varude märkimise poliitika, mida soovite kasutada, kui planeeritud tellimused on kinnitatud.
    - **Peata kinnitamine, kui ilmneb tõrge** – Seadke see suvand valikule *Jah*, et peatada kõigi valitud planeeritud tellimuste kinnitamine, kui ühes neist ilmneb tõrge. See valik peab olema seatud *Ei*, kui suvand **Paralleelne kinnitamine** on seatud valikule *Jah*.
    - **Paralleelne kinnitamine** – See suvand on saadaval ainult siis, kui [*Planeeritud tellimuste paralleelne kinnitamise* funktsioon](#enable-features) on süsteemis sisse lülitatud ja te olete valinud kinnitamiseks kaks või rohkem planeeritud tellimust. Seadistage see väärtusele *Jah*, et käivitada kinnitamisprotsess paralleelselt. Paralleelne kinnitamine võib parandada jõudlust.
    - **Lõimede arv** – See suvand on saadaval ainult siis, kui [*Planeeritud tellimuste paralleelne kinnitamise* funktsioon](#enable-features) on süsteemis sisse lülitatud ja te olete seadnud valikule **Paralleelne kinnitamine** *Jah*. Sisestage kinnitamisprotsessi paralleelseks kasutamiseks lõimede arv. Lisateavet selle kohta, kuidas seda suvandit üldplaneerimises kasutada, vt [koondplaneerimise jõudluse parandamine](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Parameetri **Lõimede arv** säte *0* (null) pikendab üldplaneerimise töötamise aega. Seetõttu soovitame sellele väljale alati määrata väärtuse, mis on suurem kui 0.

    - **Grupeeri hankija järgi** – Määrake selle suvandi väärtuseks *Jah*, et grupeerida planeeritud ostutellimusi ja luua kinnitades ühe ostutellimuse hankija kohta. Võite ka luua ühe ostutellimuse, kus on iga planeeritud tellimuse kohta eraldi rida.
    - **Grupeeri ostjate järgi grupp** – Valige selle suvandi puhul *Jah*, kui soovite plaanitud ostutellimused grupeerida, et luua üks ostutellimus, kus on ühendatud hankijate ja sisseostjate grupid. Selle suvandi kasutamiseks peate valima ka suvandi **Grupeeri hankija järgi** puhul *Jah*.
    - **Grupeeri perioodi järgi** (jaotises **Ostutellimused**) – Valige periood, mille järgi plaanitud ostutellimusi grupeerida. Selle suvandi kasutamiseks peate valima ka suvandi **Grupeeri hankija järgi**.
    - **Grupeeri perioodi järgi** (jaotises **Ülekanded**) – Valige periood, mille järgi plaanitud ülekandeid grupeerida. Tellimused grupeeritakse väärtuste alusel **Laost** ja **Lattu**.

    ![Parameetrite kiirvalik kinnitamise dialoogiaknas](./media/manual-firming.png "Parameetrite kiirvalik kinnitamise dialoogiaknas")

1. Seadistage **Töö taustal** käitamine kiirkaardil nii, et see töötaks pakett-režiimis. Korduvat ajakava pole aga mõtet käsitsi kinnitamise ajal paika panna. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul. Käsitsi kinnitamiseks töötleb pakett-töö ainult hetkel valitud planeeritud tellimusi. See ei töötle ühtegi tellimust, mis sobiks filtritega, mida praegu leheküljel rakendatakse.
1. Valige **OK**, et rakendada oma sätted ja luua kinnitatud tellimused.

## <a name="auto-firm-planned-orders"></a>Planeeritud tellimuste automaatne kinnitamine

Automaatkinnitamine võimaldab teil kinnitada planeeritud tellimused üldplaneerimise protsessi osana. Võite määratleda kindla ajaakna katvusrühmade, üksikute üksuste ning üksuste ja üldplaanide kombinatsioonide jaoks. Seejärel määratakse plaanitud tellimused üldplaneerimise käitamise ajal automaatselt, kui tellimuse kuupäev jääb kinnitamiseks määratud ajapiiri piiresse. Plaanimise optimeerimise loodud planeeritud tellimused ja integreeritud üldplaneerimise toiming käsitsevad tellimuse kuupäeva (st alguskuupäeva) teisiti.

> [!NOTE]
> Planeeritud ostutellimuse automaatkinnitamine saab aset leida ainult siis, kui üksus on hankijaga seotud.
> 
> Tuletatud tellimused (st alltöövõtulepingute ostutellimused), mis on kinnitatud, on staatuses *Ülevaatamisel*, kui muudatuste jälgimine on sisse lülitatud.

> [!IMPORTANT]
> Enne kui selles jaotises kirjeldatud funktsiooni saab kasutada plaanimise optimeerimisega, peab [*Plaanimise optimeerimise automaatne kinnitamise* funktsioon](#enable-features) olema teie süsteemis sisse lülitatud, nagu on kirjeldatud selle teema alguses. Automaatset kinnitamist saab alati kasutada integreeritud üldplaneerimise mootoriga.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automaatne kinnitamine planeerimise optimeerimise vs integreeritud planeerimise mootoriga

Nii planeerimise optimeerimist kui ka sisseehitatud planeerimismootorit saab kasutada planeeritud tellimuste automaatseks kinnitamiseks. Kuid on ka olulisi erinevusi. Näiteks kui planeerimise optimeerimine kasutab tellimuse kuupäeva (s.o alguskuupäev), et määrata, millised planeeritud tellimused kinnitada, siis sisseehitatud planeerimismootor kasutab vajaduse kuupäeva (s.o lõppkuupäev). Järgmine tabel võtab erinevused kokku.

| | Planeerimise optimeerimine | Integreeritud plaanimismootor |
|---|---|---|
| **Kuupäeva alus** | Automaatne kinnitamine põhineb tellimuse kuupäeval (alguskuupäev). | Automaatne kinnitamine põhineb nõude kuupäeval (lõppkuupäev). |
| **Täitmisaeg** | Kuna tellimuse kuupäev (alguskuupäev) käivitab kinnituse, ei pea te täitmisaega kinnitamise aja osana arvestama. | Tellimuste tähtajaks kinnitamise tagamiseks peab kinnitamise ajapiir olema pikem kui täitmisaeg. |
| **Käimaoleva nädala tellimused** | Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema üks nädal. | Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema täitmisaeg pluss üks nädal. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Automaatse kinnitamis- ja kinnitamisajapiiri seadistamine

Lülitate automaatse kinnitamise sisse, määrates automaatse kinnitamise ajapiiri asjakohasele leviala seadistusele, nagu on kirjeldatud selles jaotises hiljem. Kui automaatne kinnitamine ei ole ühegi laovarude häälestuse jaoks sisse lülitatud või planeerimine on käivitatud kindlalt leheküljelt, nt väljastatud toote **Netonõuete** leht, jäetakse automaatne kinnitamisprotsess vahele.

Automaatseks kinnitamiseks vajalikud grupeerimis- ja märkimisvalikud võtavad oma väärtused **Üldplaneerimise parameetrite** lehe vahekaardilt **Standardne uuendamine**.

Automaatse tihendamise ajapiiri määrab päevade arv, mille sisestate vastava leviala seadistamiseks. Automaatse kinnitamise saate sisse lülitada ja kinnitamisaega juhtida järgmistel viisidel:

- Katvusgrupi vaikimisi kinnitamise ajapiiri määramiseks avage **Koondplaneerimine \> Seadistus \> Katvus \> Katvusgrupid** ja valige katvusgrupp. Seejärel sisestage kiirkaardil **Muu** väljale **Automaatse kinnitamise ajapiir (päevades)** päevade arv.
- Konkreetse kauba laovarude grupis määratletud kinnitamisajapiiri ülekirjutamiseks minge **Tooteteabe haldusse \> Väljastatud tooted**. Valige tegevuspaanilt **Plaan** ja seejärel valige **Katvusühik**. Seejärel valige vahekaardil **Üldine** suvand **Ajapiiride alistamine** ja sisestage väljale **Automaatse kinnitamise ajapiir (päevad)** päevade arv.
- Konkreetse koondplaani katvusgrupi ja laovarude haldamise jaoks määratletud kinnitamise ajapiiri ülekirjutamiseks avage **Üldplaneerimine \> Seadistus \> Üldplaanid** ja valige üldplaan. Seejärel määrake kiirkaardil **Ajapiir päevades** suvand **Kinnitamine** olekusse *Jah* ja sisestage päevade arv.

Kui seate kõigi eelnevalt nimetatud ajapiiride väärtuseks *0* (null), keelatakse vastavate kaetud kaupade puhul automaatne kinnitamine tõhusalt.

## <a name="firm-planned-orders-by-using-a-query"></a>Planeeritud tellimuste kindlad tootmistellimused päringu abil

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

Päringupõhine kinnitamine võimaldab planeerida kinnitamist eelnevalt määratletud kriteeriumide alusel. Erinevalt automaatsest kinnitamisest võimaldab päringupõhine kinnitamine automatiseerida erinevate tellimuste alamhulkade eri ajahetkedel. Lisaks saate kasutada kas käsitsi või automatiseeritud operatsioone erinevat tüüpi planeeritud tellimuste tegemiseks. Samuti saate oma sätete põhjal kuvada eelvaate selle kohta, millised kinnitatud tellimused valitakse. Seetõttu saate kinnitada, et valik vastab teie ootustele.

Saate automaatset kinnitamist kombineerida päringupõhise kinnitamisega. Näiteks päringupõhisel kinnitamise tööl on edasisuunalise aja ajapiir, mis on sobiva automaatse kinnitamise katvuse konfiguratsiooni jaoks ajapiirist pikem. Seetõttu töötleb päringupõhine kinnitamistöö oma planeeritud tellimusi enne automaatse kinnitamise käivitamist. Seda käitumist saate kasutada konkreetsete müüjate tellimuste ajastamiseks erinevalt kui teiste hankijate sarnaste toodete tellimused.

> [!IMPORTANT]
> Enne kui selles jaotises kirjeldatud funktsiooni saab kasutada peab [*Plaanimise optimeerimise automaatne kinnitamise* funktsioon](#enable-features) olema teie süsteemis sisse lülitatud, nagu on kirjeldatud selle teema alguses.

Planeeritud tellimuse kinnitamiseks päringupõhise kinnitamisprotsessi abil järgige neid samme.

1. Avage **Üldplaneerimine \> Üldplaneerimine \> Käita \> Planeeritud tellimuste kinnitamine**.
1. Seadke dialoogiboksi **Plaanitud tellimuse kinnitamine** kiirkaardil **Parameetrid** põhitöötlus-, märgistus- ja grupeerimissuvandid. Need valikud töötavad nagu dialoogiboksis **Kinnitamine**. (Kirjeldusi vt eelmisest jaotisest.) Seejärel seadke jaotises **Plaan** järgmised väljad, mis on dialoogiboksis **Plaanitud tellimuse kinnitamine** kordumatud:

    - **Plaan** – Valige üldplaan, mis tuleb rakendada selle päringuga leitud planeeritud tellimuste kinnitamisel.
    - **Kinnitamise ajapiir edasistel päevadel** – Valige, kui kaugele tulevikku peab üldplaneerimine erinevad nõuded ja muud asjaolud arvutama.
    - **Kinnitamise ajapiir eelnevatel päevadel** – Valige, kui kaugele minevikku peab üldplaneerimine erinevad nõuded ja muud asjaolud arvutama.

    ![Parameetrite kiirvalik Planeeritud tellimuste kinnitamise dialoogiaknas](./media/planned-order-firming-main-1.png "Parameetrite kiirvalik Planeeritud tellimuste kinnitamise dialoogiaknas")

1. Täpsustamaks, milliseid kirjeid tellimusse kaasatakse, valige **Filter** nupp **Kirjete valimine** kiirvalik. Kuvatakse standardne päringudialoog, kus saate määrata valikukriteeriumid, sortimiskriteeriumid ja ühendamised. Väljad töötavad samamoodi nagu muudel päringutüüpidel Supply Chain Management puhul. Siinsed väljad on kirjutuskaitstud ja kuvavad teie päringuga seotud väärtused.

    ![Kirjete kiirvalik Planeeritud tellimuste kinnitamise dialoogiaknas](./media/planned-order-firming-main-2.png "Kirjete kiirvalik Planeeritud tellimuste kinnitamise dialoogiaknas")

1. Valige **Eelversioon**, et vaadata kinnitatud tellimuse sisu, mis baseerub teie senistel seadetel. Sõnumina kuvatakse planeeritud tellimuste loetelu, mis kinnitatakse. Seejärel saate oma sätteid vastavalt vajadusele reguleerida, kuni eelversioon näitab kindlat järjekorda nii, nagu soovite.

    ![Näide kinnitatud tellimuse eelversioonist](./media/planned-order-firming-preview.png "Näide kinnitatud tellimuse eelversioonist")

    > [!WARNING]
    > See funktsioon kinnitab kõik filtri kriteeriumidele vastavad plaanitud tellimused. Planeeritud tellimuste mittekriitiline kinnitamine võib põhjustada tohutu hulga soovimatuid ostu-, üleandmis- ja tootmistellimusi. Enne jätkamist kasutage alati **Eelversioon** nuppu, et kinnitada kaasatud kirjed.

1. Seadistage **Töö taustal** käitamine kiirkaardil nii, et see töötaks pakett-režiimis ja/või seadke korduv ajakava. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige **OK**, et rakendada oma sätted ja luua kinnitatud tellimused.

## <a name="track-firmed-orders"></a>Jälgige kinnitatud tellimusi

Kinnitatud planeeritud tellimuse jälgimiseks järgige neid samme.

1. [Kõigi planeeritud tellimuste loendilehe](approved-planned-order.md#view-planned-orders)avamine.
1. Valige või avage planeeritud tellimus, mida soovite jälgida.
1. Seejärel valige toimingupaanil vahekaardi **Vaade** grupis **Vaade** suvand **Kinnitamisajalugu**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
