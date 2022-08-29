---
title: Tellimuspõhise tarne automatiseerimine
description: See artikkel kirjeldab, kuidas seadistada ja kasutada erinevaid täiustusi, mis on lisatud vastavalt tellimusele tarnimise automatiseerimise funktsioonile.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220738"
---
# <a name="make-to-order-supply-automation"></a>Tellimuspõhise tarne automatiseerimine

[!include [banner](../includes/banner.md)]

Tellimusele *tarnimise automatiseerimise funktsiooniga* lisatakse Microsoftile mitu täiustust Dynamics 365 Supply Chain Management. Need täiustused võimaldavad sooritada järgmisi toiminguid.

- Vaadake kasutaja määratletud perioodi ressursi võimsuse koormust ja seetõttu lubage võimsuse koormuse pikaajaline hindamine.
- Parandada paindlikkust, kontrollides iga koondplaani viivituse kõikumise (negatiivsed päevad) arvu.
- Säilitage tooted, mis on saadaval viimase hetke tellimuste jaoks ja optimeerige olemasoleva pakkumise kasutamist, sidumisega nõudlusele kõige värskem võimalik pakkumine, selle asemel et kasutada esimest võimalikku tarnet.
- Säilitage pärast kinnitamist tootmistellimustele komponentide määramise paindlik komponent, et süsteem saaks optimeerida viimase minuti nõudluse muudatusteks. Teiste sõnadega, piira märkimist ühe tasemeni.
- Kontrollige iga müügitellimuse täitmispoliitikat. Vaikesätted võetakse kliendiseadistusest.
- Täiustage kontsernisisest teabevoogu. Ostutellimused uuendatakse nii, et need sisaldaks tarneviisi, tarnetingimuste ja välise kaubakoodi välju. See muudatus tagab, et üksikasjalik nõudluse teave võib muutuda tarneettevõttele.

See artikkel kirjeldab, kuidas seadistada ja kasutada iga täiustust.

> [!NOTE]
> Kõik selles artiklis kirjeldatud täiustused kehtivad süsteemide puhul, mis kasutavad integreeritud koondplaneerimist. Planeerimise optimeerimise lisandmoodul Microsofti jaoks toetab ka järgmisi täiustusi Dynamics 365 Supply Chain Management.
>
> - Lükka koondplaanide kõikumine edasi
> - Koondplaneerimisel kasutatud sidumisjärjestuse kontroll

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Tellimusele tarnimise automatiseerimise funktsiooni sisse lülitumine

Enne kui saate selles artiklis kirjeldatud funktsiooni kasutada, peate selle süsteemi jaoks sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, kus see funktsioon on järgmisel viisil loetletud:

- **Moodul: koondplaneerimine** *·*
- **Funktsiooni nimi:** *tellimusele tarnimise automatiseerimine*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Häälestage võimsuse koormuse lehel kuvamispäevade arv.

Võimsuse **koormuse** leht võimaldab teil ressursi saadaoleva võimsuse üle vaadata. Tellimusele *tarnimise automatiseerimise funktsioon* parandab võimsuse **koormuse lehte**, lisades **päevade** arvu välja. Selle välja abil saate piirata päevade arvu, mida näitab **ülevaateruudustik**. Teie seatud väärtus salvestatakse mälus. Seega, kui lahkute lehelt ja hiljem tagasi pöördute, **kuvatakse** ülevaate ruudustikus siiski viimati määratud päevade arv.

Et avada võimsuse **koormuse** leht nii, et saate üle vaadata konkreetse ressursi saadaoleva võimsuse, järgige neid samme.

1. Minge organisatsiooni **halduse ressurssidesse \>\>**.
1. Valige kontrolliv ressurss.
1. Valige tegevuspaani vahekaardi **Ressurss** jaotises Vaade **suvand** Võimsuse **koormus**.
1. Kasutage filtrit **Päevade** arv, et piirata päevade arvu, mida ülevaate **ruudustik** näitab.

Et avada võimsuse **koormuse** leht nii, et saate ressursigrupi saadaoleva võimsuse üle vaadata, järgige neid samme.

1. Avage **Organisatsiooni haldus \> Ressursid \> Ressursigrupid**.
1. Valige kontrolliks ressursigrupp.
1. Valige tegevuspaani vahekaardil **Ressursigrupp** grupis Vaade **suvand** Võimsuse **koormus**.
1. Kasutage filtrit **Päevade** arv, et piirata päevade arvu, mida ülevaate **ruudustik** näitab.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Rakenda plaanitud tellimuste kinnitades märgistuse üksiktase

*Märkimist* kasutatakse pakkumise ja nõudluse linkimiseks. See meenutab *sidumist*, mis näitab, kuidas koondplaneerimise abil soovitakse nõudlusele vastata. Märkimine on siiski sidumisest püsivam. Tellimusele *tarnimise automatiseerimise funktsiooniga* lisatakse võimalus piirata varude märkimine plaanitud tellimuste kinnitamist üksiktasemele. See lisab plaanitud tellimuse **kinnitades** **dialoogiboksi** Märkimise värskendamine väljale Järgmised uued valikud:

- *Ühetasemeline* – kasutatakse ühetaseme märkimist. Ühetasemeline märgistus märgib ainult põhikaupa, mitte selle koosluse komponente. Seetõttu saate pärast kinnitamist säilitada tootmistellimuste komponentide määramise paindlikuna. Ühetasemeline märkimine võimaldab süsteemil optimeerida viimase minuti nõudluse muudatusi. Standardses *ühetaseme* märkimises märgitakse vajaduse tellimused nende täitmistellimustele vastamiseks, kuid täitmistellimusi ei märgita, kui nende kogus on järelejääv.
- *Ühetasemeline laiendatud* – kasutatakse ühetaseme märkimist. Laiendatud *ühetasemeline* märgistus näitab vajadusetellimusi nende täitmistellimustega seoses ja täitmistellimused märgitakse alati, olenemata sellest, kas mingi kogus jääb alles.

Need valikud on **saadaval** **ka koondplaneerimise parameetrite vahekaardi Standardne** **uuendamine** väljal Märkimine, **kus saate määratleda dialoogiboksi Kinnitamist** vaikevaliku.

Lisateavet vt varude märkimisest [plaanimise optimeerimisega](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Sea viivituse kõikumine (negatiivsed päevad) koondplaani tasemel

Tellimusele *tarnimise automatiseerimise funktsiooni abil* saab konfigureerida viivituskõikumist (negatiivseid päevi) koondplaani tasemel. Säte on saadaval ka kauba laovarude ja laovarude grupi tasemetel. Kui negatiivsed päevad on määratud rohkem kui ühel tasemel, rakendab süsteem järgmise hierarhia otsustamaks, millist sätet kasutada:

- Kui negatiivsed päevad on koondplaanide **lehel** konfigureeritud, alistab see säte kõik teised negatiivsete päevade sätted plaani käitamisel.
- Kui negatiivsed päevad on konfigureeritud kauba **laovarude** lehel, alistab see säte laovarude grupi sätte.
- Laovarude gruppide lehel konfigureeritud negatiivsed **päevad** kehtivad ainult juhul, kui vastava kauba või koondplaani jaoks pole negatiivseid päevi konfigureeritud.

Koondplaani negatiivsete päevade miseks järgige neid samme.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige loendipaanil koondplaan või looge uus.
1. Seadke ajapiiride **päevade** kiirkaardil suvandi **Negatiivsed päevad väärtuseks** *Jah*.
1. Sisestage lähedalasuv väljale lubatud negatiivsete päevade arv.

Lisateavet negatiivsete päevade kasutamise kohta vt Viivituse kõikumine [(negatiivsed päevad)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Koondplaneerimisel kasutatava sidumisjärjestuse juhtimine

Koondplaneerimine kasutab sidumisjärjestust *määramaks*, milline pakkumine katab millist nõudlust. Tellimusele *tarnimise automatiseerimise funktsiooniga* **lisatakse** uus valik Kasuta viimast võimalikku tarnet, mis annab teile kontrolli sidumise järjestuse üle. Uus valik võimaldab teil säilitada viimaste minutite tellimuste jaoks saadaolevaid tooteid ja optimeerida olemasoleva pakkumise kasutamist, sidumisega nõudlusele viimast võimalikku pakkumist, selle asemel et kasutada esimest võimalikku tarnet.

Sidumisjärjestuse saate seada koondplaani, kauba laovarude või laovarude grupi tasemel. Kui sidumisjärjestus seadistatakse rohkem kui ühel tasemel, rakendab süsteem järgmist hierarhiat otsustamaks, millist sätet kasutada:

- Kui sidumisjärjestus on koondplaanide **lehel** seadistatud, alistab see säte plaani käitamisel kõik muud sidumisjärjestuse sätted.
- Kui sidumisjärjestus on kauba laovarude lehel **seadistatud**, alistab see säte laovarude grupi sätte.
- Lehel Laovarude grupid seadistatud sidumisjärjestus kehtib ainult juhul, kui sidumisjärjestuse sätted ei ole **vastava** kauba või koondplaani jaoks konfigureeritud.

Sidumise häälestamiseks laovarude grupi tasemel järgige neid samme.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Laovarude grupid**.
1. Valige loendipaanil grupp või looge uus.
1. Sidumisjärjestuse **jaotise** **·** **·** **Üldine** kiirkaardil kasutage sidumisjärjestuse konfigureerimiseks välju Tarbi vaba kaubavaru ja Kasutage oma sidumisjärjestuse konfigureerimiseks viimaseid tarnevälju. Selles jaotises allpool toodud tabel näitab, kuidas need sätted on ühendatud teie sidumisjärjestuse määratlemiseks.

Sidumise häälestamiseks kauba laovarude tasemel järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige ruudustikus toode või looge uus.
1. Valige tegevuspaani vahekaardil **Plaan kauba laovarud** **.**
1. Kauba **laovarude** leht sisaldab ridu, mis lasevad teil määratleda laovarude reeglid, mis kehtivad kaubale igas laos. Valige ruudustikus olemasolev rida või looge uus.
1. **Märkige vahekaardil** Üldine ruut **Alista sidumisjärjestus**.
1. Kasutage sidumisjärjestuse **konfigureerimiseks** välju Tarbi **vaba** kaubavaru ja Kasuta uusimaid tarnevälju. Selles jaotises allpool toodud tabel näitab, kuidas need sätted on ühendatud teie sidumisjärjestuse määratlemiseks.

Sidumise häälestamiseks koondplaani tasemel järgige neid samme.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige loendipaanil koondplaan või looge uus.
1. Seadke kiirkaardi **Üldine** sidumisjärjestuse **alistamise suvandi väärtuseks** *Jah*.
1. Kasutage sidumisjärjestuse **konfigureerimiseks** välju Tarbi **vaba** kaubavaru ja Kasuta uusimaid tarnevälju. Selles jaotises allpool toodud tabel näitab, kuidas need sätted on ühendatud teie sidumisjärjestuse määratlemiseks.

Järgmine tabel näitab, kuidas tarbimis **vaba kaubavaru ja** **Kasuta** viimaseid tarnesätteid on ühendatud, et luua oma sidumisjärjestus.

| | Kasuta viimast tarnet = Jah | Kasuta viimast tarnet = Ei |
|---|---|---|
| **Tarbi vaba kaubavaru enne** = *kogu tarnimist* | <ol><li>Laoseis</li><li>Olemasolev pakkumine, mis vastab nõudluse kuupäevale</li><li>Olemasolev pakkumine, mis ei vasta nõudluse kuupäevale, kuid jääb siiski negatiivsete päevade piiresse</li><li>Uue tarne loomine (plaanitud tellimus)</li></ol> | <ol><li>Laoseis</li><li>Olemasolev pakkumine, mis vastab nõudluse kuupäevale</li><li>Olemasolev pakkumine, mis ei vasta nõudluse kuupäevale, kuid jääb siiski negatiivsete päevade piiresse</li><li>Uue tarne loomine (plaanitud tellimus)</li></ol> |
| **Tarbi vaba kaubavaru pärast** = *kogu tarnimist* | <ol><li>Olemasolev pakkumine, mis vastab nõudluse kuupäevale</li><li>Laoseis</li><li>Olemasolev pakkumine, mis ei vasta nõudluse kuupäevale, kuid jääb siiski negatiivsete päevade piiresse</li><li>Uue tarne loomine (plaanitud tellimus)</li></ol> | <ol><li>Olemasolev pakkumine, mis vastab nõudluse kuupäevale</li><li>Olemasolev pakkumine, mis ei vasta nõudluse kuupäevale, kuid jääb siiski negatiivsete päevade piiresse</li><li>Laoseis</li><li>Uue tarne loomine (plaanitud tellimus)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Vaadake üle ja määrake igale müügitellimusele rakenduv täitmispoliitika

Täitmispoliitikad kontrollivad tellimuse koguhinna või koguse protsenti, mis tuleb enne müügitellimuse lattu väljalaset füüsiliselt reserveerida. Saate seada globaalse vaikimisi täitmispoliitika ja seejärel selle konkreetsete klientide jaoks vastavalt vajadusele alistada. Tellimusele *tarnimise automatiseerimise* funktsiooniga lisatakse võimalus vaadata, millist vaikepoliitikat tegelikult mis tahes tellimusele rakendada ja rakendada tellimuseomast alistamist vastavalt vajadusele.

- Müügitellimuste globaalse täitmispoliitika vaikeväärtuse seadistamiseks minge müügireskontro seadistuse **müügireskontro \>\> parameetritele**. Seejärel seadistage **laohalduse** vahekaardil **müügitellimuse täitmispoliitika** väli poliitika nimele, mida soovite kasutada. 
- Kliendispetsiifilise müügitellimuste täitmispoliitika miseks minge müügireskontro **klientide \> kõigi klientide \> väljadele**. Seejärel seadistage **vahekaardil** Ladu täitmispoliitika **väli poliitika nimele,** mida soovite kasutada.

Vaikepoliitika vaatamiseks, mis rakendub mis tahes tellimusele ja tellimusepõhine alistamine, järgige neid samme.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Avage müügitellimus, mida soovite üle vaadata või redigeerida.
1. Valige **päisevaade**.
1. Vaadake üle **ja** redigeerige lao kiirkaardil järgmised väljad vastavalt vajadusele.

    - **Tellimuse täitmise poliitika** – valige valitud tellimuse puhul kasutamiseks täitmispoliitika. Vaikepoliitika alistatakse. Vaikimisi täitmispoliitika kasutamiseks, mis kuvatakse täitmispoliitika **vaikeväärtuse väljal**, jätke see väli tühjaks.
    - **Täitmise vaikepoliitika** – sellel väljal kuvatakse täitmise **vaikepoliitika, mis rakendub, kui tellimuse täitmise poliitika väli** on tühi. See väli on kirjutuskaitstud. Kui see väli on tühi, ei määratleta kliendiomast ega globaalset vaike täitmispoliitikat.

    Kui nii **tellimuse täitmispoliitika** väli **kui ka täitmispoliitika vaikepoliitika** väli on tühjad, siis täitmispoliitikat ei rakendu. Ent kehtestatud võivad olla muud piirangud ja need võivad nõuda reserveeringute või muude tingimuste täitmist enne müügitellimuse vabastamist.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Tarneviisi ja -tingimuste lülitamine üksikutele ostutellimuse ridadele

Kõik ostutellimused sisaldavad **tellimuse** päises **tarnetingimusi** ja tarneviisi sätteid. Tellimusele *tarnimise automatiseerimise funktsiooniga* lisatakse need sätted igale tellimusereale. Seega saate mis tahes või kõigi tellimuseridade **jaoks** määrata tarnetingimuste ja/**või** tarneviisi väärtuse avate vastavalt vajadusele. Ridade puhul, kus alistamist ei määratleta, kasutatakse päise väärtust. Saate määrata, kas tellimuse päise ühe või mõlema välja väärtuse muudatus peaks samuti kõiki ridu uuendama.

Selleks, et määratleda, mis toimub rea **sätetega**, kui kasutaja muudab tarnetingimusi ja/**või** tarneviisi väärtust tellimuse päises, järgige neid samme.

1. Minge **Hanked \> Seadistus \> Hangete parameetrid**.
1. **Valige tellimuseridade** uuendamise **link vahekaardi Üldine kiirkaardil** **Vaikeväärtused ja parameetrid**.
1. **Valige dialoogiboksi Tellimuseridade** uuendamine väljadel **Tarnetingimuste** **värskendamine** ja Tarneviisi värskendamine üks järgmistest väärtustest:

    - *Mitte* kunagi – ärge kunagi uuendage tellimuse ridu pärast sätete muutmist tellimuse päises.
    - *Alati* – uuendage alati kõiki tellimuseridu pärast sätete muutmist tellimuse päises.
    - *Viip* : kui kasutaja muudab tellimuse päises üht või mõlemat sätteid, avage dialoogiaken, kus küsitakse, kas kasutaja soovib kõiki ridu uuendada nii, et need ühtiksid muudatusega ühe või mõlema seadistusega.

Tarneteabe ostutellimuse päisele seatud, järgige neid samme.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Avage ostutellimus, mida soovite redigeerida.
1. Valige **päisevaade**.
1. Seadke tarnerežiimi **ja** tarnetingimuste väljad **tarne kiirkaardil** **vastavalt** vajadusele.
1. Olenevalt hankeparameetrite **lehe** sätetest võidakse teilt küsida, kas soovite oma muudatused rakendada kõigile tellimuse ridadele.

Ostutellimuse rea tarneteabe akseste etappide järjekorra miseks järgige neid samme.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Avage ostutellimus, mida soovite redigeerida.
1. Valige ridade **vaade**.
1. **Valige ostutellimuse ridade** kiirkaardil redigeeritav rida.
1. Seadke vahekaardi **Tarne** rea üksikasjade kiirkaardil **nõutavad** **väljad Tarneviis** **ja Tarnetingimused**. Ühtivate sätete kasutamiseks päises tühjendage üks või mõlemad väljad.

Kontsernisiseste tellimuste **puhul** **sünkroonitakse** iga ostutellimuse rea tarneviisi ja tarnetingimuste väljade väärtused ostutellimuse ja sellega seotud müügitellimuse vahel.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Sünkrooni kontsernisiseste tellimuste välised kauba ID-d ja kirjeldused

Kontsernisiseste tellimuste puhul lubab funktsioon Teha tellimusse tarnimise automatiseerimise funktsioon välised kauba ID-d *ja tekstikirjeldused ostutellimuse ridadel sünkroonida seotud kontsernisiseste müügitellimuste ridadega, sõltumata sellest,* kas ostutellimus on otsetarne ks. See funktsioon lisab võimaluse määrata kontsernisisesel ostutellimusel ka lõplik väliskliendi konto. Süsteem võtab seejärel (sisemise) kontsernisisese hankija kirje asemel väliskliendi kirjest automaatselt väliskauba ID-d ja teksti kirjeldused.

Kontsernisisese hankija sünkroonimiseks kontsernisiseste ostutellimuste ja nendega seotud müügitellimuste väliste kaubakoodide ja kaubanimede vahel järgige neid samme.

1. Avage **Hanked \> Hankijad \> Kõik hankijad**.
1. Saate valida seadistada kontsernisisese hankija.
1. Valige kontsern tegevuspaani **vahekaardi** Üldine jaotises **Seadistus** **·**.
1. Märkige **kontsernisisese** **·** **lehekülje vahekaardi Ostutellimuse tekstiväljal kontsernisisese ostutellimuse -\>** **kontsernisisese müügitellimuse jaotises ruut Väline kauba ID** ja kauba nimi.

Kontsernisisese ostutellimuse lõpliku välise kliendikonto määramiseks järgige neid samme. Väli **Kliendi konto** kehtib ainult kontsernisiseste ostutellimuste puhul. Selle välja abil saate määrata selle kliendi kontonumbri, kes kaubad lõpuks vastu võtab. Kui see väli on määratud, võetakse ostutellimuse ridadel määratud kliendikontolt välised kaubakirjeldused ja numbrid ostutellimusel määratud kontsernisisese hankija asemel. Kui muudate kliendi kontot hiljem, uuendatakse välised kaubakirjeldused ja ID-d nii, et need ühtivad uue konto väärtustega. Iga rea välised kaubakirjeldused ja ID-d sünkroonitakse samuti vastava kontsernisisese müügitellimusega.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Avage ostutellimus, mida soovite seadistada või looge uus.
1. Valige **päisevaade**.
1. Seadke jaotises **Viide** väljale Kliendi konto **vastav** väliskliendi konto.

Väliste kauba ID-de ja tekstikirjelduste määramiseks kontsernisisese tellimuse ostutellimuse reale järgige neid samme. Seadistatud väärtused sünkroonitakse seotud kontsernisisese müügitellimuse ridadega, sõltumata sellest, kas ostutellimus on otsetarneks või mitte.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Avage ostutellimus, mida soovite seadistada või looge uus.
1. Valige ridade **vaade**.
1. **Valige ostutellimuse ridade** kiirkaardil redigeeritav rida.
1. **Kiirkaardi** **Rea** üksikasjad vahekaardi Üldine **jaotises** **Tellimuse** rida väljal Tekst sisestage valitud tellimuse real määratud kauba väline kirjeldus. See väärtus sünkroonitakse seotud kontsernisisese müügitellimuse reaga.
1. **Jaotise Viide** väljal **Väline** sisestage valitud tellimusereal määratud kaubale väline kauba ID. See väärtus sünkroonitakse seotud kontsernisisese müügitellimuse reaga.

Lisateavet vt teemast Kontsernisisese [müügitellimuse loomine ja arveldamine väliskliendi jaoks](../sales-marketing/intercompany-sales-order-for-external-customer.md).
