---
title: Lattu väljastamine
description: See artikkel annab üksikasju lattu vabastamise protsessi kohta. See kirjeldab üksusi, mis luuakse tellimuse vabastamisel lattu ja valikuid, mida saate protsessi käivitamiseks kasutada.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c3280b2e39d7af5ca99cad703cad6ecc7b307bff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893174"
---
# <a name="release-to-warehouse"></a>Lattu väljastamine

[!include [banner](../../includes/banner.md)]

See artikkel annab üksikasju lattu vabastamise protsessi kohta. See kirjeldab üksusi, mis luuakse tellimuse vabastamisel lattu ja valikuid, mida saate protsessi käivitamiseks kasutada.

## <a name="release-to-warehouse-overview"></a>Lattu väljastamise ülevaade

Lattu välja saatmine on varude lähetuseks valmis panemise protsess. Kui vabastate tellimuse lattu, loob süsteem koormaread ja saadetised. Kui voo automaatne töötlemine on seadistatud, luuakse ka koormad ja nõutud töö. Kaasatud üksuste konfiguratsioon sõltub süsteemi sätetest. See artikli jaotis vaatab üle lattu vabastamise protsessi ajal loodud üksused ja neid määratlevad süsteemisätted.

*Saadetis* on sama kliendi või sama tarneaadressi müügitellimuse või üleviimistellimuse ridade grupp.

*Koorem* on rühm müügitellimuste või üleviimistellimuste ridu, mis on grupeeritud tavaliselt ühele veoautole, rööbassõidukile või muule transpordiviisile. Koormal võib olla üks või mitu saadetist. Koorma saate käsitsi luua, lisades tellimusread uude koormasse. Sel juhul määratakse tellimuse read koormale enne lattu vabastamise protsessi käivitamist ja neid saab vabastada ainult **Koorma planeerimise töö** laualt.

Lao *töö* on iga laotöö, mida teostab laotöötaja. Tavaliselt koosnevad lao töö toimingud vähemalt paarist tegevusest: laotöötaja komplekteerib ühes kohas vaba kaubavaru ja viib komplekteeritud kaubavarud teise kohta.

Kui tellimused lattu väljastatakse, loob süsteem *koormaread* ja rühmitab need saadetisteks. Saadetise konsolideerimisprotsess võimaldab lattu vabastamise protsessis automatiseeritud saadetise konsolideerimist. Lisateabe saamiseks vt [Saadetiste konsolideerimise poliitikad](about-shipment-consolidation-policies.md).

Süsteem kasutab *laineid* komplekteerimistöö ja saadetise koormate loomiseks. *Voomall* peab olema saadaval seda tüüpi voo jaoks, mida soovite luua ja tellimuse rea lao jaoks. Müügitellimuste ja ülekandekorralduste esemete *Saatmiseks* kasutage saatmistüübi laine malli.

Iga voomall sisaldab *voomeetodeid*. Voomeetodid sooritavad toiminguid, nagu laine jaoks töö loomine või koormate loomine. Näiteks lainete saatmise laine mall võib sisaldada meetodeid koormuste loomiseks, joonte eraldamiseks lainetele, täiendamiseks ja laine jaoks kogumistööde loomiseks. Voomall määrab mitu seadistust voo loomise ja töötlemise kohta, sh millised sammud tuleb teha käsitsi ja mida tehakse automaatselt. Lisateabe saamiseks vaadake jaotist [Voomallid](wave-templates.md). Seega, sõltuvalt voomalli konfiguratsioonist, luuakse, töödeldakse ja vabastatakse voo tellimuse lattu vabastamisel automaatselt või teostatakse pärast lattu väljast väljasadmist mõned või kõik need tegevused käsitsi.

Voo töötlemisel loob süsteem sobiva *töömalli* ja *asukohadirektiivi* põhjal komplekteerimistöö ning teeb töö mobiilsetes seadmetes kättesaadavaks. Töömall määrab, kuidas iga laoprotsessi puhul tööd tehakse ning asukohadirektiiviga määratakse laoliikumise jaoks komplekteeritud ja panemiskohad. Lisateavet vaadake teemast [Laotöö juhtimine töömallide ja asukohadirektiividega](control-warehouse-location-directives.md).

> [!NOTE]
> Laineid töödeldakse vaikimisi pakkrežiimis.

Voo töötlemise ajal loob süsteem tavaliselt uue koormuse igale saadetisele, millele pole koormust määratud. Kui soovite, et süsteem määraks määramata saadetised hoopis olemasolevatele koormatele, saate kasutada täpsema laine koormuse loomise funktsiooni. Lisateavet vt teemast [Täiustatud koorma koostamine voo ajal](advanced-load-building-during-wave.md).

**Müügitellimustel** ja **üleviimistellimustel** saate üle vaadata üksused, mis on loodud tellimuse ridade jaoks lattu vabastamise protsessi ajal.

- **Müügitellimused** leht:

    - **Müügitellimuse ridade** kiirkaardil valige **Lao haldus** ja siis menüüs valige **Saadetise detailid** et avada saadetised **Koorma üksikasjad** seotud koormate avamiseks **Töö üksikasjad** et avada seotud töö üksikasjad.
    - Valige **Rea üksikasjad** kiirkaardil **Koormad** seotud koormate ülevaatamiseks.

- **Ülekandetellimuste** leht:

    - Tegevuspaani vahekaardil **Saatmine** valige **saadetise üksikasjad** seotud saadetiste avamiseks või **Koorma üksikasjad** seotud koormate avamiseks.
    - **Üleviimistellimuse** kiirkaardil valige **Töö üksikasjad** seotud töö üksikasjade avamiseks.

Kokkuvõtteks, kui tellimus vabastatakse lattu, toimib kõige automaatsem voog järgmisel viisil:

1. Süsteem loob tellimusele saadetise ja voo.
1. Voogu töödeldakse.
1. Süsteem loob koorma ja töö ID.

Sõltuvalt voo mallidest, töömallidest ja asukohadirektiivide sätetest võivad mõned sammud selles voos muutuda manuaalseks. Kuid üleüldine voog jääb samaks.

Teil on mitu valikut selle kohta, kuidas te tellimust lattu välja saadate. Seda toimingut saate teha käsitsi või seadistada pakett-töö. Selle artikli ülejäänud jaotised vaadata üksikasjalikult läbi mitmesugused viisid, kuidas saate teha lattu väljast vabastamise toimingut.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Käsitsi lattu väljaminemine müügitellimuste ja üleviimistellimuste lehtedelt

Tellimuse saate lattu välja anda otse lehelt **Müügitellimused** või **Üleviimistellimused** valides käsu **Vabasta lattu**.

- **Müügitellimuste** lehel on tegevuspaani vahekaardil nupp **Ladu**.
- **Ülekandetellimuste** lehel on tegevuspaani vahekaardil nupp **Saada**.

Leheküljel **Müügitellimused** saate korraga vabastada mitu müügitellimust.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Käsitsi lattu vabastus lehelt Väljalaskmine lattu

Süsteem pakub praegu kolme lehekülge, kus saate üle vaadata mitme tellimuse read ja vabastada need lattu:

- **Lattu väljaminek** (**Warehouse management \> lattu väljaminek \> lattu väljaminek**) - See leht võimaldab teil töötada nii müügitellimuste kui üleviimistellimustega. Kuid see võimaldab aeglasemalt jõudlust, kui ülejäänud kaks lehekülge. See lehekülg on varsti aegunud.
- **Vabastage müügitellimused lattu** (**Warehouse management \> lattu väljaminek \> müügitellimuste lattu väljaminek**) - See leht võimaldab teil töötada ainult müügitellimustega. Kuid see tagab parema jõudluse kui lehekülg **Lattu väljaminek**.
- **Vabastage üleviimistellimused lattu** (**Warehouse management \> lattu väljaminek \> üleviimistellimuste lattu väljaminek**) - See leht võimaldab teil töötada ainult üleviimistellimustega. Kuid see tagab parema jõudluse kui lehekülg **Lattu väljaminek**.

Kõik kolm lehekülge pakuvad sarnaseid funktsioone, nagu kirjeldatud selles jaotises. Kõik need lasevad teil valida tellimuseread või terved tellimused ja seejärel vabastada need lattu.

Iga lehekülg koosneb ülemisest jaotisest, kus saate valida tellimuse ridu ja alumist sektsiooni, kus saate käivitada vabastamise lattu protsessi. Vabastada soovinud müügitellimuse ridade otsimiseks saate kasutada ülemise jaotise filtreid. **Lattu vabastamise** lehel on ülemises jaotises müügitellimuste ja üleviimistellimuste jaoks eraldi vahekaart, kuid ülejäänud kaks lehekülge tellimust näitavad ainult üht tüüpi .

Ülemise jaotise tööriistariba hõlmab järgmisi nuppe, mida saate kasutada tellimusridade valimiseks lattu vabastamiseks:

- **Lisa** - Valige ülemises jaotises üks või mitu tellimuserida ja seejärel valige see nupp neile ridadele alumises jaotises.
- **Lisa kõik** – lisage kõik read ülemisest jaotisest alumisesse jaotisesse.
- **Lisa tellimus** - Valige tellimus ja seejärel valige see nupp, et lisada kõik selle tellimuse read alumisesse jaotisesse.

Kui olete ridade lisamise alumisele jaotisele lõpetanud, märkige kõik vabastatud read. Seejärel valige **vabastamine lattu** tööriistaribal, et vabastada need read lattu.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Käsitsi väljastamine lattu lehelt Koorma plaanimise töölaud

Saate tellimused lattu ka käsitsi välja vabastada, kasutades lehte **Koorma plaanimise töölaud**. See lehekülg võimaldab teil korraldada tellimuse read koormatele ja seejärel vabastada need koormad lattu.

Avage **Koormuse plaanimise töölaud** leht, minge **Warehouse management \> Koormad**. Samuti saate seda avada lehtedel **Müügitellimused** ja **Üleviimistellimused**. Lehe ülemises jaotises saate valida müügitellimuse read vahekaardil **Müügiread** ja üleviimistellimuse read vahekaardil **Üleviimisread** ning seejärel lisada need read uude või olemasolevasse koormasse.

Tegumiriba vahekaart **Pakkumine ja nõudlus** sisaldab järgmisi nuppe, mida saate kasutada koormale tellimuseridade lisamiseks ülemisesse jaotisesse:

- **Lisa uude koormasse** - Valige ülemises jaotises üks või mitu tellimuserida ja seejärel valige see nupp, et luua uus koormus ja lisade need read sellele.
- **Lisa olemasolevasse koormasse** - Valige ülemises jaotises üks või mitu tellimuserida ja seejärel valige see nupp, et lisada need olemasolevasse koormasse.
- **Kogu tellimus uude koormasse** - Valige tellimused, ja seejärel valige see nupp, et luua uus koorem ja lisade sellele kõik read sellest tellimusest.
- **Kogu tellimus olemasolevasse koormasse** - Valige tellimus, ja seejärel valige see nupp, et lisada kõik read sellest tellimusest.

Alumises jaotises saate üle vaadata loodud koormad. Valige jaotise Koormused tööriistaribal koormuse lattu väljastamiseks **Väljasta \> Lattu väljastamine**. Kui kasutate voo automaatset töötlemist, kuna koormad on juba tellimuse ridadele määratud, loob süsteem lattu vabastamise toimingu ajal saadetised ja töö ID-d.

## <a name="automatic-release-to-the-warehouse"></a>Automaatne väljastamine lattu

Tellimuste lattu automaatseks vabastamiseks kasutage **müügitellimuste automaatset vabastamist** ja **üleviimistellimuste automaatatse väljalaske** töid.

Müügitellimusi vabastava pakett-töö häälestamiseks tehke järgmist.

1. Avage jaotis **Laohaldus \> Lattu väljastamine \> Müügitellimuste automaatne väljastamine**.
1. Seadke dialoogiboksis **Automaatne müügitellimuse väljalase** kiirkaardil **Parameetrid** järgmised väljad:

    - **Vabastav kogus** - Valige, kas partiina tuleks väljastada terve kogus või füüsiliselt reserveeritud kogus.
    - **Luba osaliselt väljastatud tellimuste väljalase** - määrake, kas osaliselt väljastatud tellimuste järelejäänud kogused tuleb lattu välja vabastada.
    - **Säilita vabastuse tõrke reserveerimised** – Määrake, kas müügitellimuse jaoks automaatselt reserveeritud kogused tuleb reserveeridakui lattu vabastamise protsess nurjub.
    - **Väljalasete grupeerimine** klientide kaupa – määrake, kas süsteem peaks iga kliendi puhul töötlema väljalaset eraldi lattu või vabastama samaaegselt kõik müügitellimused. Kui see suvand on seatud *valikule* Jah, kogub süsteem kõik valitud kliendi müügitellimuse read, vabastab need tellimused lattu ja töötleb seejärel järgmise kliendi. Kui see suvand on seatud valikule *Ei*, vabastab süsteem kõik saadaolevad müügitellimuse read ühe laotoiminguna. Selle suvandi lubamisega saate aidata parandada laosse vabastamise protsessi jõudlust ja soovitud tulemusi. Peate olema siiski ettevaatlik, kui kasutate seda suvandit koos voomallidega, mis on konfigureeritud töötlema laineid lattu vabastamisel, sest see kombinatsioon võib luua palju ühe kliendi laineid, millest igaühel on töö, mis on loodud ainult sellele kliendile. Kui soovite luua töö, mis ühendab saadetisi mitmele kliendile, *peate* kas välja lülitama grupi väljaminekud kliendi suvandi järgi või konfigureerima oma voomallid edasilükatud töötluse kasutamiseks.
    - **Lukustatud tellimuste käsitsemine** – Valige, kuidas süsteem peaks käsitlema praegu lukustatud müügitellimusi, kuna neid redigeerivad teised kasutajad või protsessid:

        - *Oota, kuni tellimused vabastatakse* - Süsteem peaks ootama, kuni tellimused vabastatakse, enne kui see need lattu vabastab. Sel juhul võib lattu vabastamise protsess võtta rohkem aega.
        - *Lukustatud tellimuste vahelejätmine* – süsteem peaks lukustatud tellimused vahele jäetma.

    - **Kehtivad etllimusetüübid** - Valige partiisse kaasamiseks müügitellimuste tüübid.
    - **Krediidilimiidi tüüp** – valige, kas krediidilimiite tuleb lattu vabastamise protsessi käigus kontrollida ja kas kontrolli tuleks teha ka nendesse kaasamiseks kandeteave.

1. Et kontrollida, milliseid tellimusi töödelda, valige kiirkaardil **kaasavad kirjed** suvand **Filtreeri**. Kuvatakse standardne päringudialoog, kus saate määrata valikukriteeriumid, sortimiskriteeriumid ja ühendamised. Väljad töötavad samamoodi nagu muudel päringutüüpidel Microsoft Dynamics 365 Supply Chain Management puhul.
1. Seadistage **Töö taustal käitamine** kiirkaart nii, et see töötaks pakett-režiimis ja/või seadke korduv ajakava. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige **OK** oma sätete rakendamiseks ning et käivitada vabastamine laoprotsessile.

Üleviimistellimusi vabastava pakett-töö häälestamiseks tehke järgmist.

1. Avage jaotis **Laohaldus \> Lattu väljastamine \> Üleviimistellimuste automaatne väljastamine**.
1. Seadke dialoogiboksis **Automaatne üleviimistellimuse väljalase** kiirkaardil **Parameetrid** järgmised väljad:

    - **Vabastav kogus** - Valige, kas partiina tuleks väljastada terve kogus või füüsiliselt reserveeritud kogus.
    - **Luba osaliselt väljastatud tellimuste väljalase** - määrake, kas osaliselt väljastatud tellimuste järelejäänud kogused tuleb lattu välja vabastada.
    - **Grupeerib vabastused sihtlao alusel** – määrake, kas süsteem peaks kõik üleviimistellimused samaaegselt välja vabastama või grupeerima üleviimistellimuse read sihtlao järgi ja seejärel vabastama iga grupi eraldi lattu.

1. Et kontrollida, milliseid tellimusi töödelda, valige kiirkaardil **kaasavad kirjed** suvand **Filtreeri**. Kuvatakse standardne päringudialoog, kus saate määrata valikukriteeriumid, sortimiskriteeriumid ja ühendamised. Väljad töötavad samamoodi nagu muudel päringutüüpidel Supply Chain Management puhul.
1. Seadistage **Töö taustal käitamine** kiirkaart nii, et see töötaks pakett-režiimis ja/või seadke korduv ajakava. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige **OK** oma sätete rakendamiseks ning et käivitada vabastamine laoprotsessile.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
