---
title: Toote töötsükli olekud ja kanded
description: Selles teemas selgitatakse, kuidas saate kontrollida, millised kanded on igas töötsükli olekus lubatud, kui tehniline toode töötsüklit läbib.
author: t-benebo
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1e9b8a9f25edfa654a57e0ab4071cd93c8033d85
ms.sourcegitcommit: d375ef4138e898621416754c40770d8ccca4d271
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8322740"
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

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Välja lastud toodete ja tootevariantide elutsükli olekud

Tootel, millel on variandid (põhi ja variandid), on tootel (põhi) elutsükli olek ja igal variandil võib olla ka erinev elutsükli olek.

Kindlate protsesside puhul, kui variant või toode on blokeeritud, on protsess samuti blokeeritud. Et teha kindlaks, kas protsess on blokeeritud, kontrollib süsteem järgmist:

- Tehnikakontrolliga toodete puhul:
  - Kui praegune tehnika versioon on blokeeritud, blokeerige protsess.
  - Kui praegune versioon on blokeeritud, blokeerige protsess.
  - Kui praegune toote väljalase on blokeeritud, blokeerige protsess.
- Standardtoodete puhul:
  - Kui praegune versioon on blokeeritud, blokeerige protsess.
  - Kui praegune toote väljalase on blokeeritud, blokeerige protsess.

Oletame näiteks, et soovite müüa ainult ühe variandi (punane) antud tootest (t-särk) ja blokeerida kõigi teiste variantide müügi praegu. Võite seda rakendada, kasutades järgmist seadistust:

- Määrake tootele elutsükli olek, mis lubab protsessi. Määrake näiteks t-särki toote elutsükli olekuks *Müüdav*, mis lubab *Müügitellimust* äriprotsessis.
- Määrake müüdavale variandile protsessi võimaldav elutsükli olek. Määrake näiteks punasele variandile elutsükli olek *Müüdav*.
- Kõigile muudele variantidele määratakse teine elutsükli olek, kus protsess on blokeeritud. Määrake näiteks valge variandi (ja kõik muud variandid) elutsükli olekuks *Pole müüdav*, mis blokeerib blokeerib *Müügitellimuse* äriprotsessi.

## <a name="default-product-lifecycle-states"></a>Toote töötsükli vaikeolekud

Tehnikaversiooni vaikimisi töötsükli olek on määratud tehnika kategoorias. Olekut kasutatakse vaikimisi uue tehnikaversiooni, k.a uue toote esimese versiooni loomisel.

Uue toote või inseneritoote loomisel saate määrata ka töötsükli vaikeoleku, määrates selle tootele määratud väljalaskepoliitika mallil.

Sellisel juhul on tootel uue tehnikatoote loomisel võimalik omada versioonist erinevat töötsükli olekut.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
