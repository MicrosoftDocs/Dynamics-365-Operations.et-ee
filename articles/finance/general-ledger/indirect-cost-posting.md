---
title: Kaudse kulu sisestamine
description: See teema selgitab, kuidas sisestada kaudseid kulusid, luua kulugruppe ja lisada kaudsete kulude kululehele sõlmesid.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d7f4753f69d83d172993e1c9b04be2220fdf253f
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804640"
---
# <a name="indirect-cost-posting"></a>Kaudse kulu sisestamine

Kaudsed kulud on kulud, mis ei ole tootmisprotsessis otseselt seotud ühegi tegevusega. Näited hõlmavad selliseid administratiivkulusid, nagu töötajate palgad, osakonna raamatupidamiskulud ja üldkulud, nt rent, kommunaalkulud ja masinate kulud.

## <a name="calculating-indirect-costs"></a>Kaudsete kulude arvutamine

Microsoft Dynamics 365 Finantsil pole automaatset viisi kaudsete kulude määra arvutamiseks. Te peate määratlema oma kaudsed kulud, looma kaudse kulu koodid ja säilitama iga kaudse kulu määra kuluarvestuslehel.

Täpne protsess, mida kasutatakse kaudsete kulude arvutamiseks, võib ettevõtteti veidi erineda. Üldiselt koosneb protsess siiski järgmistest põhietappidest:

1. Looge tootmises äratundmiseks kaudsete kulude loend. See loend võib sisaldada rentimis-, administratiivkulusid, raamatupidamistasusid ja juriidilisi tasusid. See ei tohi sisaldada toormaterjali kulusid ega töökulusid, mida tootmisprotsessides tunnustatakse.
2. Summeerige kõik kaudsed kulud. Saate kaudseid kulusid grupeerida või üksteisest eraldada. Igal konfigureeritud kaudsel kulul võivad olla erinevad põhikontod, mida kasutatakse pearaamatusse sisestamiseks.
3. Võrrelge kaudseid kulusid teguriga, mida nimetatakse ka absorbtsiooni aluseks. See tegur võib olla mis iganes te valite. Siin on toodud mõned tavalised näited:

    - Tulu
    - Kogu toodetud kogus
    - Seadistusaeg
    - Käitusaeg

    Saate valida perioodi, mille kohta soovite kaudseid kulusid arvutada, nt kuu, kvartal või aasta. Teie kaudsete kulude summa ja teguri summa peaksid olema samal ajasummal. Kaudse kulu määra arvutamiseks kasutatakse järgmist valemit:

    *Kaudsete kulude määr* = *Kaudsete kulude kogusumma*&divide;*tegur*

4. Kaudsete kulugruppide loomine.
5. Konfigureerige kuluarvestuse leht oma määrasid.
6. Säilitage oma kaudsete kulude kulu kuluversioonis.

> [!NOTE]
> Saate kasutada kuluarvestuse **moodulit**, et koguda kulusid ja määrata oma üldkulusid erinevatest allikatest, nt tootmisest, projektidest ja pearaamatust. Lisateavet vt teemast [Kuluarvestus](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Erinevad regulatiivsed tegevuskohad on avaldanud juhised kulude tüüpide kohta, mida saab lisada kaudsete kuludena või üldkuludena teie lõpetatud kaupade hinnas. Enne kaudsete kulude konfigureerimise käivitamist soovitame teil kontrollida oma raamatupidaja ja kohalike seadustega, et tagada nende ühildumine.

## <a name="create-cost-groups-for-indirect-costs"></a>Kaudsete kulude kulugruppide loomine

Kaudsete kulude kasutamiseks peate looma vähemalt ühe kulugrupi. Puudub piirang kulugruppide arvule, mida saate kasutada. Kaaluge, kuidas te oma kulusid arvutate ja kas on olemas erinevate kulutüüpide puhul erinevad määrad. Näiteks toodab teie organisatsioon toiduainetetooteid. Mõned toormaterjalid ja valmiskaubad on kuivkaubad ning neil on ladustamiseks üks kaudne kulu. Muud toormaterjalid ja valmiskaubad lõpetatakse ning neil on suurem kaudne kulu. Sel juhul võite soovida luua kaks kulugruppi: **kuiva materjali üldkulu ja** **soovitud materjali üldkulud**.

Kaudsete kulude kulugrupi loomiseks järgige neid samme.

1. Minge tootmisjuhtimise **seadistuse protsesside &gt;&gt; kulugruppidesse&gt;**.
2. Grupi **loomiseks** valige väärtus Uus.
3. Sisestage **kulugrupile** kordumatu nimi **, näiteks MA SISESTAMAH**.
4. **Sisestage väljale** Nimi kulugrupi kirjeldus, nt Materjali **üldkulud**.
5. Valige väljal **Kulugrupi** tüüp suvand **Kaudne**.
6. Valikuline: väljal **Käitumine** valige fikseeritud **kulu või** muutuvkulu **·**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Kaudsete kulude kuluarvestuse lehe konfigureerimine

Kui olete loonud ühe või mitu kulugruppi, saate konfigureerida oma kaudsete kuludega kuluarvutustabeli ja määratleda oma arvutuse. Võite soovida grupeerida kaudseid kulusid kuluarvestuslehel. Kaudsete kulude grupeerimiseks saate kuluarvestuslehel luua valikulise päise. Iga kulugrupi jaoks tuleb kuluarvestuslehel luua vähemalt üks sõlm. Iga kaudse kulugrupi jaoks saate lisada veel ühe kaudse kulu kalkulatsiooni.

### <a name="indirect-cost-node-types"></a>Kaudse kulu sõlmetüübid

Selles jaotises kirjeldatakse kaudsete kulude sõlmede erinevaid tüüpe.

#### <a name="surcharge"></a>Lisatasu

**Lisatasu** on üks kaudsete kulude kõige tavalisemaid tüüpe. See arvutab kulu protsendi tootmistellimuse kulude absorbtsiooni põhjal. Määratlege absorbtsiooni alus, valides kulutabelis oma materjali või ajakomponentidega seotud kulugrupid.

Näiteks võidakse tootmistellimus kõigi toormaterjalide tootmiskulule lisada 3-protsendist lisatasu.

#### <a name="rate"></a>Määr

Määra tüübi kaudset **kulu** kasutatakse tootmistellimusele fikseeritud kulusumma lisamiseks tootmistellimuse kulude absorbtsiooni alusel. Määr võib põhineda ühel kolmest alamtüübist:

- **Protsess** – määr põhineb protsessi käitusajal.
- **Seadistus** – määr põhineb protsessi seadistusajal.
- **Kogus** – määr põhineb toodetud kogusel.

Määratlege absorbtsiooni alus, valides kulutabelis materjali või aja komponentidega seotud kulugrupid.

Näiteks lisatakse igale tootmistellimusele fikseeritud summa 2,00 USD- (USD), mis põhineb kulutabeli tööjõu kulugrupi protsessi käitusajal.

#### <a name="output-unit-based"></a>Väljundüksusel põhinev

Toodangu ühikul **põhineva tüübi** kaudne kulu arvutatakse, korrutades summat, mis on **määratletud** kuluarvestuse lehe kiirkaardil valitud alamtüübiga. Saate kaudse kulu teguriks valida lõpetatud kauba koguse, kaalu või mahu.

Te kasutate näiteks kogust masina 1.50 USD iga toodetud koguse kohta kulumi arvutamiseks. Teise näitena kasutate mahtu, et 2.00 USD kirjelduskulusid ruumi mahu kohta, mida lõpetatud kaubad teie mõõtuühikutes võtavad.

#### <a name="input-unit-based"></a>Sisestusüksusel põhinev

Sisendühikul põhineva **kaudse kulu tüübi** arvutamiseks korrutatakse tootmistellimusel tarbitava toormaterjali summaga. Kogusumma arvutamiseks saate kasutada tootmistellimuse sisendite kaalu või mahtu. Saate piirata kalkulatsiooni materjalide alamkogumiga, **valides kuluarvutustabeli kiirkaardil Absorbtsiooni** alusel ühe või mitu kulugruppi.

Näiteks saate tootmistellimusse lisakulude lisamiseks kasutada kindla kulugrupi sisestuste mahtu, mis on seotud 1.00 USD toodetega.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Kaudsete kulude kogusõlme loomine kuluarvestuse lehel

Kaudsete kulude kogusõlme loomiseks kuluarvestuslehel järgige neid samme.

1. Minge kuluhalduse **kaudse kuluarvestuse &gt; poliitika seadistuse kuluarvestuse &gt; lehele**.
2. Valige puus sõlm, mis näitab toodetud kaupade kulu.
3. Sõlme **loomiseks** valige väärtus Uus.
4. Valige väljal **Sõlme tüübi** valimine suvand **Kokku**.
5. Sisestage **koodiväljale** sõlme kordumatu ID, nt tootmise **üldkulud**.
6. Märkige ruut **Päis**.
7. Märkige ruut **Kokku**.
8. Valige nupp **OK**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Kaudse kulugrupi sõlme loomine kuluarvestuslehel

Kaudse kulugrupi sõlme loomiseks kululehel järgige neid samme.

1. Minge kuluhalduse **kaudse kuluarvestuse &gt; poliitika seadistuse kuluarvestuse &gt; lehele**.
2. Valige puus sõlm, mille alla soovite kaudse kulu luua. Valige näiteks tootmise üldkulude **kogusõlm**.
3. Sõlme **loomiseks** valige väärtus Uus.
4. **Valige väljal Sõlme tüübi** valimine suvand **Kulugrupp**.
5. Sisestage **koodiväljale** sõlme kordumatu ID, nt **TRANSP**.
6. Sisestage **kirjeldusväljale** lühikirjeldus, nt transpordi **üldkulud**.
7. Valige nupp **OK**.
8. Valige kulugrupi **väljal** kulugrupp, nt **OVH1: transpordi üldkulud**.

### <a name="create-a-surcharge-indirect-cost"></a>Lisatasu kaudse kulu loomine

Et luua oma kululehel lisatasu kaudne kulu, järgige neid samme.

1. Minge kuluhalduse **kaudse kuluarvestuse &gt; poliitika seadistuse kuluarvestuse &gt; lehele**.
2. Valige puus kaudse kulu grupi sõlm, mille alla soovite kaudse kulu luua. Näiteks valige kogusõlm TRANSP - **Transpordi üldkulud jaoks**.
3. Sõlme **loomiseks** valige väärtus Uus.
4. Valige lisamaksu **väljal Sõlme** tüübi **valimine**.
5. Sisestage **koodiväljale** sõlme kordumatu ID, nt transpordi **lisatasu**.
6. Valige nupp **OK**.
7. Valige väljal **Alamtüüp** suvand **Kokku**.
8. Kulukoodi **loomiseks** valige kiirkaardil **Absorbtsiooni** alusel väärtus Uus.
9. **Valige väljal** Kood kulugrupp, mida kasutada lisatasu arvutamiseks.
10. Valikuline: korrake samme 8 kuni 9 iga täiendava kulugrupi puhul, mida soovite kalkulatsioonis kasutada.
11. Lisatasu kiirkaardil **valige** määra **loomiseks** uus.
12. **Valige väljal** Versioon kuluversioon, millele lisatasu lisada.
13. Valikuline: sisestage **saidi** väljale sait, mille puhul lisatasu rakendada.
14. Sisestage **väljale** Protsent protsent, mida arvutada tootmistellimustel kulugruppidest, mis **on määratletud kiirkaardil Absorbtsiooni** alus.
15. Valige kiirkaardil Pearaamatu sisestused **põhikonto,** mida kasutada hinnangulise kaudse kulu jaoks, **tarbitud kaudsete kulude hinnanguline omahind,** lõpetamata tarbimine, **kaudse kulu väljad ja tarbitud kaudse kulu kulu, lõpetamata** toodangu **väljad** **.**
16. Valikuline: **määrake kiirkaardil** Finantsdimensioonid mis tahes finantsdimensioonid, mida pearaamatusse sisestamisel vaikimisi kannetele sisestada.

Eelnev protseduur näitab, kuidas luua lisatasu tüüpi kaudseid **kulusid**. Sarnaseid samme kasutatakse ka teiste kaudsete kulude tüüpide loomiseks. Järgmised jaotised kirjeldavad iga tüübi erinevusi.

#### <a name="rate"></a>Määr

- 4. sammus valige **lisatasu** asemel **määr**.
- 7. sammus valige Summa asemel protsess, seadistus **või** **kogus**.**·** **·**
- Kasutage 11. sammus lisatasu **kiirkaardi** asemel kiirkaarti **Määr**.
- Sammus 14 sisestage summa **väljale Summa**, mitte protsent **väljale** Protsent.

#### <a name="output-unit-based"></a>Väljundüksusel põhinev

- Sammus 4 valige lisatasu **asemel väljundühik** **·**.
- 7. sammus valige **summa** asemel **kogus**, **kaal** või **maht**.
- Jätte vahele etapid 8 kuni 10.
- Kasutage 11. sammus lisatasu **kiirkaardi** asemel kiirkaarti **Määr**.

#### <a name="input-unit-based"></a>Sisestusüksusel põhinev

- Sammus 4 valige lisatasu **asemel sisendühik** **·**.
- 7. sammus valige **summa asemel** **kaal** või **maht**.
- Kasutage 11. sammus lisatasu **kiirkaardi** asemel kiirkaarti **Määr**.
