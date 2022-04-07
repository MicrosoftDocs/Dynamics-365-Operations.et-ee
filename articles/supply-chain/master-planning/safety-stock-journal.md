---
title: Puhvervaru abil üksuste minimaalse laovaru uuendamine
description: See teema kirjeldab, kuidas kasutada ohutusvaru töölehte kaupade puhul ohutusvaru koguse uuendamiseks, arvutades ajaloolistel kannetel põhinevaid minimaalse laovaru ettepanekuid.
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 391f741ee08eb0624e80f5c297009c527e50c14c
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468534"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Puhvervaru abil üksuste minimaalse laovaru uuendamine

[!include [banner](../../includes/banner.md)]

Ohutusvaru näitab laos hoitava kauba lisakogust, et vähendada riski, et kaup laost välja läheb. Puhvervaru kasutatakse puhvrina juhul, kui müügitellimused on kasutatavad, kuid hankija ei saa kliendi nõutavale lähetuskuupäevale vastata.

See teema kirjeldab, kuidas kasutada laovaru töölehte, et arvutada minimaalsed laovarude ettepanekud, mis põhinevad ajaloolistel kannetel, ja seejärel uuendada kauba laovarud vastavalt taotlustele.

## <a name="overview-of-minimum-coverage-usage"></a>Laovarude miinimumkasutuse ülevaade

Iga kauba jaoks seadistatakse laovaru **kauba** laovarude lehel. Varude täiendamise eri tüüpe esindavad erinevad laovarude koodid. (Lisateavet vt teemast [Kaupade laovarude täitmine.](safety-stock-replenishment.md)) Kõik laovarude koodid kasutavad siiski väärtust, mis on **seadistatud** **iga kauba laovarude lehel** miinimumväljale. Minimaalse välja kasutamisel on kaks peamist **lähenemist**:

- **Miinimumkogus miinimum-/maksimumeesmärkidel** – see lähenemine kasutab miinimumkogust koos min/max loogikaga. See rakendub, kui **vastava kauba** või laovarude *grupi puhul on välja Laovarude kood väärtuseks seatud Min/* Max. Minimaalne **kogus** tähistab keskmist päevakasutust, mis on korrutatud kauba täitmisajaga.
- **Minimaalne kogus laoplaani eesmärkidel – see lähenemine kasutab minimaalset kogust, et esindada varude plaani kombinatsioonis** nõudluse prognoosidega. See rakendub, kui **vastava kauba** või laovarude *grupi puhul* on *välja Laovarude* kood väärtuseks seatud Periood või Vajadus. Minimaalne **kogus** tähistab laoplaani, mis kajastab soovitud klienditeeninduse taset, et vähendada laost väljaregistreerimise, osaliste saadetiste ja tarne täitmisaeg. Minimaalne kogus peegeldab prognoosi täpsuse protsenti antud kauba puhul. See ei tähista soovitud laoseisu.

Miinimumväärtuse **saate** seadistada kolmel viisil:

- Käsitsi kauba laovarude **lehel**
- Andmehalduse raamistiku alusel (kauba *laovarude* andmeüksused)
- Ohutusvaru töölehtede tehtud arvutuse järgi

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Minimaalse laovarude arvutamine ajaloolise kasutuse põhjal

Ohutusvaru töölehti kasutatakse pakutud miinimumkoguse arvutamiseks, võttes aluseks kauba ajaloolise kasutuse (kas minimaalsel/maksimaalsel eesmärgil või laoplaani eesmärgil). Ajalooline kasutus tähistab kõiki väljaminekukandeid määratud perioodil. Need väljaminek kanded hõlmavad müügitellimuse kandeid ja lao korrigeerimisi. Arvutustega tuvastatakse ka pakutud miinimumkoguse mõju laoväärtusele ja laoväärtuse muutus võrreldes praeguste miinimumkogustega.

Iga ohutusvaru töölehe rida tähistab kaupa ja selle laovarude dimensioone. Need tööleheread luuakse ja kuvatakse ohutusvaru töölehe **ridade lehel (** koondplaneerimise käita ohutusvaru **\>\>\> kalkulatsioon).** Selles teemas kirjeldatakse äriprotsessi, mille puhul kasutatakse ohutusvaru töölehti soovitatud miinimumkoguste arvutamiseks.

Planeerija kasutab valitud kaupade jaoks soovitatud miinimumkoguste arvutamiseks ohutusvaru töölehte, võttes aluseks valitud perioodide ajaloolise kasutamise. Soovitatud miinimumid saab vajaduse korral käsitsi alistada ja saate üle vaadata pakutud miinimumide potentsiaalset mõju laoväärtusele. Töölehe sisestamisel uuendatakse automaatselt seostatud miinimumkogused kauba laovarudes.

### <a name="create-a-new-safety-stock-journal-name"></a>Uue puhvervaru töölehe nime loomine

Seda tüüpi töölehe loomiseks peate looma vähemalt ühe ohutusvaru töölehe nime. Tavaliselt võite kasutada mitut töölehe nime, mis aitavad ohutusvaru kalkulatsioone eraldada.

1. Minge koondplaneerimise **ohutusvaru \>\> töölehe nimede juurde**.
1. Valige toimingupaanil nupp **Uus**.
1. Seadke uuel real järgmised väljad:

    - **Nimi** : sisestage töölehe lühinimi.
    - **Kirjeldus** : sisestage töölehe kirjeldus.
    - **Privaatne kasutajagrupile** – praeguse töölehenime sihtgrupi piiramiseks valige kasutajagrupp.
    - **Kustuta read pärast** sisestamist – märkige see ruut töölehe ridade vaikimisi puhastamiseks nende sisestamisel. Tühjendage see, kui soovite kõik sisestatud read säilitada.

    Töölehe **tüübi väli** on kirjutuskaitstud ja on eelseadistatud väärtusele *Ohutusvaru*.

1. Sulgege leht.

### <a name="create-a-safety-stock-journal-and-lines"></a>Ohutusvaru töölehe ja ridade loomine

See samm loob töölehe ja lisab sellele read automaatselt. Iga rida tuvastab kauba, selle laovarude dimensioonid ja mitu arvutatud kogust kasutusajaloost. Arvutatud kogused hõlmavad keskmiseid väljaminekuid kauba täitmisaja, keskmise väljamineku ja kuu standardhälbe kohta.

#### <a name="automatically-generate-journal-lines"></a>Loo töölehe read automaatselt

Tööleheridu saab automaatselt luua ainult siis, kui töölehel pole praegu kuvatud ridu.

Järgige neid samme tööleheridade automaatseks loomiseks.

1. Minge koondplaneerimise **koondplaneerimise \> käitama \> ohutusvaru \> arvutusse**.
1. Valige toimingupaanil nupp **Uus**. Luuakse uus ohutusvaru tööleht.
1. Seadke töölehe **päise üksikasjade** kiirkaardil järgmised väljad:

    - **Nimi** : valige ohutusvaru töölehe nimi, millele rida lisada.
    - **Kirjeldus** – vaikeväärtus on valitud töölehe nime kirjeldus. Kuid te saate seda väärtust vajaduse korral redigeerida.
    - **Kustuta read pärast sisestamist** – märkige see ruut tööleheridade puhastamiseks nende sisestamisel. Tühjendage see, kui soovite kõik sisestatud read säilitada. Säte pärineb valitud töölehe nimest.

    **Töölehe** väli on kirjutuskaitstud ja sellel kuvatakse selle töölehe ID-kood, millega ridu loote ja lisate.

1. Valige tööleheridade **kiirkaardil** **tööriistaribal** käsk Loo read.
1. Seadke dialoogiboksis **Tööleheridade loomine pakutud minimaalse** kaubavaru tasemete jaoks järgmised väljad:

    - **Alguskuupäev**: valige perioodi alguskuupäev, mille väljaminekud tuleks arvutamisse kaasata.
    - **Lõppkuupäev** : valige perioodi lõppkuupäev, mille väljaminekud tuleks selle arvutamisse kaasata. Algus- ja lõppkuupäeva vahel peab olema vähemalt kaks kuud.
    - **Arvuta standardhälve** – määrake selle valiku väärtuseks *Jah,* et arvutada standardhälve. Kui soovite soovitust arvutades *kasutada* suvandit Kasuta **teenusetaset**, tuleb selle suvandi väärtuseks seada Jah (vt kirjeldust käesolevas teemas allpool).

1. Kiirkaarti **kaasatavatel** kirjetel saate seadistada filtrid ja piirangud, et määrata, millised kaubad kaasatakse. (Näiteks saate filtreerida **Laovarude grupi** väärtus.) Valige **filter**, et avada standardpäringu redaktori dialoogiboks, kus saate määratleda valikukriteeriumid, sortimiskriteeriumid ja liitmised. Väljad töötavad nii nagu Microsoft muud tüüpi päringute puhul Dynamics 365 Supply Chain Management.
1. Valige taustal **tehtud kiirkaardil**, kas käitada töö pakett-režiimis ja/või seadistada korduv graafik. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige nupp **OK**. Read luuakse dimensioonidele, kus on laokanded.

#### <a name="manually-add-or-remove-journal-lines"></a>Tööleheridade käsitsi lisamine või eemaldamine

Tööleheridu saate igal ajal käsitsi lisada ja/või eemaldada (kas ridade automaatse loomise järel või selle asemel). Kasutage töölehe ridade kiirkaardi tööriistaribal **järgmisi** nuppe:

- **Uus** – saate lisada uue rea. Seejärel sisestage igasse veergu väärtus, et määrata toode, mille jaoks uusi miinimume arvutada ja rakendada. Kuna soovitatud miinimumkalkulatsioonid pole käsitsi lisatud ridade puhul saadaval, ei kuvata nende jaoks **uusi arvutatud miinimumkoguse** väärtusi. Seetõttu peate käsitsi sisestama uued miinimumkoguse **väärtused**. Saate siiski vaadata uue **miinimumkoguse** väärtuse potentsiaalset mõju laoväärtusele ja laovarude potentsiaalset muutust võrreldes praegu täpsustatud miinimumiga.
- **Kustuta** – kustutage valitud rida.
- **Kustuta töölehe read** : kustutage kõik töölehe read.

### <a name="calculate-a-proposal"></a>Arvuta soovitus

See samm arvutab igale töölehe reale soovitatud miinimumi ja rea võimaliku mõju laoväärtusele. (Pakutav miinimum kuvatakse järgmiselt: **Arvutatud miinimumkoguse** väärtus.) Kalkulatsioone saate vajaduse korral teha mitu korda. Kalkulatsioon uuendab **kõigi tööleheridade** puhul kuvatava arvutatud miinimumkoguse väärtuse.

Kuvatavad arvutused ei mõjuta iga toote tegelikke minimaalse koguse väärtusi enne, kui valite tegevuspaanil **valiku** Sisesta. Sel ajal rakendatakse **igale tootele** uued miinimumkoguse väärtused.

1. Minge koondplaneerimise **koondplaneerimise \> käitama \> ohutusvaru \> arvutusse**.
1. Avage tööleht, mille jaoks soovitust arvutada. Teise võimalusena looge uus tööleht, nagu selles teemas varem kirjeldatud.
1. Valige tööleheridade **kiirkaardil** tööriistaribal **suvand** Arvuta soovitus. (Te ei pea ühtegi rida valima.)
1. Seadke dialoogiboksis **Minimaalse kaubavaru taseme arvutamise** dialoogiboksis järgmised väljad:

    - **Kasutage keskmist väljaminekut** täitmisaja **jooksul** – tehke see valik, et luua arvutatud minimaalse koguse väärtused, mis põhinevad määratud perioodi keskmisel väljaminekul. Seejärel sisestage **väljale Korrutustegur** väärtus, mida soovite vajaduse korral korrigeerida. Näiteks sisestage *1,0* täpse arvutatud *keskmise kasutamiseks või 1,1* 10-protsendise lisapuhvri lisamiseks.
    - **Kasuta teenuse taset** – valige see suvand, et arvutada pakutav miinimum soovitud teenusetaseme alusel. Seejärel valige väljal **Teenustase** eelistatud teenusetase.
    - **Täitmisaja** brutokasum – sisestage väärtus, mis pikendab tavalist täitmisaega (nt administreerimis võimaldamiseks).
    - **Kasutage arvutatud miinimumkogust uue** minimaalse kogusena –*·* **määrake see valik valikule Jah, et kopeerida väärtused automaatselt veerust Arvutatud miinimumkogus** **kõigile** ridadele pärast kalkulatsiooni lõpetamist. Kui seadistate valiku väärtuseks *Ei*, **kopeeritakse** praegune miinimumkoguse väärtus kõigi **ridade veergu** Uus miinimumkogus. Seejärel peate vajadusel redigeerima käsitsi uusi **minimaalse koguse** väärtusi.

1. Valige taustal **tehtud kiirkaardil**, kas käitada töö pakett-režiimis ja/või seadistada korduv graafik. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige nupp **OK**. Kalkulatsiooni tulemused kuvatakse kiirkaardi **Töölehe read** veerus **Arvutatud miinimumkogus**. Praegu on väärtused ainult pakutavad väärtused, mida pole teie toodetele veel rakendatud.

### <a name="update-minimum-quantity"></a>Miinimumkoguse uuendamine

Saate valida mis tahes rea ohutusvaru töölehel ja alistada käsitsi selle välja Uue **minimaalse koguse** väärtuse.

1. Minge koondplaneerimise **koondplaneerimise \> käitama \> ohutusvaru \> arvutusse**.
1. Avage redigeeritav tööleht. Teise võimalusena looge uus tööleht, nagu varem kirjeldatud.
1. Leidke töölehe **ridade** kiirkaardil korrigeeritav rida ja redigeerige seejärel väärtust veerus Uus **miinimumkogus**. Näiteks võite seada uue miinimumkoguse **väärtuse nii**, et see vastaks arvutatud **miinimumkoguse väärtusele**. Kui arvutatud **miinimumkoguse väärtus** on *0* (null), saate sisestada soovitud tulevase väärtuse.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Uue miinimumkoguse sisestamine ja tulemuse kinnitamine

Järgige neid samme uue miinimumkoguse sisestamiseks ja tulemuse kinnitamiseks.

1. Minge koondplaneerimise **koondplaneerimise \> käitama \> ohutusvaru \> arvutusse**.
1. Avage tööleht, mille jaoks sisestada uued miinimumkogused. Teise võimalusena looge uus tööleht, nagu varem kirjeldatud.
1. Tehke toimingupaanil valik **Väljastamine**.
1. Seadke dialoogiboksis **Töölehe** sisestamine väli Kanna kõik sisestusvead **üle uuele tööleheväljale**, nagu on nõutud. Seejärel valige **töölehe sisestamiseks OK**.
1. Kui muutsid **töölehe ridade** kiirkaardi rea **uut** minimaalse koguse väärtust, saate muudatuse kinnitada järgmiste sammude abil:

    1. Valige redigeeritud rea jaoks link veerus **Kaubakood**.
    1. Dialoogiaknas **Tooteteave** valige link väljal **Kaubakood**, et avada seotud väljastatud tootekirje.
    1. Toimingupaani vahekaardil **Plaan** rühmas **Laovarud** valige suvand **Kauba laovarud**.
    1. Pange tähele, **et minimaalne** väärtus saidile ja laole, mida korrigeerisite sisestatud ohutusvaru töölehe abil, on nüüd värskendatud nii, et see sobiks teie redigeerimisega.

## <a name="additional-resources"></a>Lisaressursid

- [Kaupade puhvervaru täitmine](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
