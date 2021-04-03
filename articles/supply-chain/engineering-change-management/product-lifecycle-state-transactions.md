---
title: Toote töötsükli olekud ja kanded
description: Selles teemas selgitatakse, kuidas saate kontrollida, millised kanded on igas töötsükli olekus lubatud, kui tehniline toode töötsüklit läbib.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9c6ba9831b84e1220ee158d8186675107b490124
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266171"
---
# <a name="product-lifecycle-states-and-transactions"></a>Toote töötsükli olekud ja kanded

[!include [banner](../includes/banner.md)]

Tähtis on, et saaksite kontrollida, millised kanded on igas töötsükli olekus lubatud, kui tehniline toode töötsüklit läbib. Näiteks ei tohi tooteid, mis pole veel küpses olekus, panna müügitellimusele. Teise võimalusena, kui toode jõuab tööea lõpu olekusse, on mõistlik kontrollida selle toote sissevoolu.

Tehnilise toote puhul on töötsükli oleku muudatused seotud toote tehniliste versioonidega. Seetõttu saab toote töötsükli olekut ühendada ka selle tehniliste versioonidega. Kui toote töötsükli olek on ühendatud tehnilise versiooniga, saate kasutada töötsükli olekut, et kontrollida, millised kanded on tehnilise versiooni puhul lubatud.

## <a name="create-and-manage-product-lifecycle-states"></a>Toote töötsükli olekute loomine ja haldamine

Toote töötsükli olekutega töötamiseks valige **Tehniline haldus \> Häälestus \> Toote töötsükli olek**. Seejärel järgige üht neist sammudest.

- Uue töötsükli oleku loomiseks valige tomingupaanil nupp **Uus** ja seejärel häälestage väljad, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva töötsükli oleku redigeerimiseks valige see loendipaanil, valige toimingupaanil nupp **Redigeeri** ja seejärel häälestage väljad nii, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva töötsükli oleku kustutamiseks valige see loendipaanil ja valige seejärel toimingupaanil nupp **Kustuta**.

> [!NOTE]
> Tehnilised tooted kasutavad samu toote töötsükli olekuid nagu tavalised (mittetehnilised) tooted. Lisaks saate avada selles teemas kirjeldatud lehe **Toote töötsükli olek**, valides **Tooteteabe haldus \> Häälestus \> Toote töötsükli olek**. Lisateavet toote töötsükli olekute kohta nii tehniliste toodete kui ka tavaliste toodete korral leiate teemast [Toote töötsükli olekute ülevaade](../pim/product-lifecycle.md).

### <a name="header"></a>Päis

Häälestage järgmised väljad tehnilise toote töötsükli oleku päises.

| Field | Kirjeldus |
|---|---|
| Maakond | Saate sisestada tehnilise toote töötsükli oleku nime. |
| Kirjeldus | Saate sisestada tehnilise toote töötsükli oleku kirjelduse. |

### <a name="general-fasttab"></a>Kiirkaart Üldine

Määrake kiirkaardil **Üldine** järgmised väljad.

| Field | Kirjeldus |
|---|---|
| Vaikimisi juriidilisele isikule väljastamisel | Tavaliste toodete puhul määrake sellele suvandile väärtus *Jah*, kui see on esmakordsel väljastamisel kõigi toodete puhul vaikimisi rakendatav. Määrake väärtuseks *Ei*, kui selle töötsükli olekut hakatakse hiljem käsitsi rakendama.<p>Seda sätet ei rakendata tehniliste toodete puhul. Tehnilise toote versiooni töötsükli olek määratakse vastavas tehnilise muudatuse kategoorias pärast seda, kui see tehnikaettevõttes luuakse. Kui toode väljastatakse aktiivsele ettevõttele, kopeeritakse toote elutsükli olek. Teisisõnu, kui tehniline toode on väljastatud aktiivsele ettevõttele, on sellel sama töötsükli olek, mis tehnilises ettevõttes. Töötsükli olekut saab aktiivses ettevõttes üle kirjutada.</p> |
| On plaanimiseks aktiivne | Määrake sellele suvandile väärtus *Jah*, et kaasata selle töötsükli olekuga tooted koondplaneerimise ja koosluse taseme arvutustesse. Määrake väärtuseks *Ei*, et välistada selle töötsükli olekuga tooted arvutustest. |

### <a name="enabled-business-processes-fasttab"></a>Lubatud äriprotsesside kiirkaart

Kiirkaarti **Lubatud äriprotsessid** saate kasutada, et kontrollida, milliseid saadaolevaid äriprotsesse saab kasutada praeguses töötsükli olekus olevate toodetega. Sellel kiirkaardil loetletud protsessid on automaatselt leitavad järgmisel viisil.

- Esimene kord, kui salvestate uue töötsükli oleku, laadib leht praegu saadaolevad äriprotsessid.
- Kui lisate oma süsteemile uusi äriprotsesse, saate kiirkaardil **Lubatud äriprotsessid** olemasoleva töötsükli oleku loendit värskendada, valides toimingupaanil käsu **Otsi värskendusi**.

Kiirkaardil **Lubatud äriprotsessid** loetletud protsesside kohta on saadaval järgmised väljad.

| Field | Kirjeldus |
|---|---|
| Töötle | See kirjutuskaitstud väli näitab olemasoleva äriprotsessi nime. |
| Protsessi ala | See kirjutuskaitstud väli näitab olemasoleva äriprotsessi valdkonda. |
| Poliis | Valige üks järgmistest väärtustest, et kontrollida, kas ja kuidas see protsess on lubatud selle töötsükliga toodete puhul.<ul><li>**Lubatud** – äriprotsess on lubatud.</li><li>**Blokeeritud** – protsess pole lubatud. Kui kasutaja püüab selle töötsükli olekuga toote korral protsessi kasutada, blokeerib süsteem katse ja kuvab selle asemel tõrketeate. Näiteks saate blokeerida tööea lõpus olevate toodete ostmise.</li><li>**Lubatud hoiatusega** – protsess on lubatud, aga kuvatakse hoiatus. Näiteks soovitakse tooteprototüüp lisada tootmistellimusele, mis on loodud uurimistöö ja arenduse osakonnas. Teistes osakonnas peaksid inimesed siiski teadma, et seda toodet ei tohi veel toota.</li></ul> |

Kui lisate kohandades veel töötsükli oleku reegleid, saate neid reegleid vaadata kasutajaliideses (UI), valides ülemisel paanil nupu **Värskenda protsessid**. Nupp **Värskenda protsessid** on saadaval ainult administraatoritele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]