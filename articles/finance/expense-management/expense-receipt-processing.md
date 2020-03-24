---
title: Kulu sissetuleku töötlemine
description: See teema annab teavet optilise märgituvastuse (OCR) kohta sissetulekute puhul. Selle funktsiooni eesmärk on parandada kasutaja kogemust, kui kuluaruandeid luuakse rakenduses Microsoftis Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113682"
---
# <a name="public-preview-expense-receipt-processing"></a>Avalik eelvaade: kulu sissetuleku töötlemine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Kulu sisestust on laiendatud optilise märgituvastuse (OCR) kaudu sissetulekute jaoks. Selle funktsiooni eesmärk on parandada kasutajakogemust, kui kuluaruandeid luuakse.

## <a name="key-features"></a>Võtmefunktsioonid

- Kaupmehe nimi, kuupäev ja kogusumma ekstraktitakse sissetulekutest.
- Funktsioon püüab vastendada sidumata sissetulekuid sidumata kulukannetega.
- Kasutajad saavad luua sissetulekutest käsitsi sisestatud kulukanded.

## <a name="usage-examples"></a>Kasutuse näited

- **Lisage automaatselt sissetulekud, mis sisaldavad krediitkaardi kandeid kuluaruande loomisel.**

    1. Avage tööruum **Kuluhaldus**.
    2. Veenduge, et vahekardil **Sissetulekud** on olemas sidumata sissetulekud. Sissetulekuid saate ka üles laadida vahekaardil **Sissetulekud**.
    3. Veenduge, et vahekardil **Kulud** on olemas sidumata kulud. Tavaliselt impordib kulu administraator need kulud krediitkaardi pakkujalt.
    4. Valige **Uus kuluaruanne**. Pange tähele, et saate kuluaruande loomisel kaasata nüüd ka kulusid ja sissetulekuid. Kui lisate nii kulusid kui sissetulekuid, käivitatakse sissetulekute automaatne sobitamine kulude alusel.

- **Looge kulu või vastendage sissetulekuga kulu.**

    1. Kuluaruande vahekaardil **Sissetulekud** saate lisada sissetuleku, valides **Lisa sissetulekud**.
    2. Sissetuleku üleslaaditud pildi all pange tähele suvandeid **Loo** ja **Vastenda**.

        - Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke sissetulekust ekstraktitud väärtused.
        - Kui valite **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.

## <a name="installation"></a>Install

See funktsioon töötab koos funktsiooniga **Kuluaruannete uuendamine**, et aidata lihtsustada kulude kogemust.

Nende täpsemate kulude võimaluste kasutamiseks installige Microsofti Dynamics 365 Finance kulude halduse lisandmoodul ja lülitage sisse funktsioonid oma eksemplaris. Saate kasutada lisandmoodulit oma projektist teenuses Microsoft Dynamics Lifecycle Services (LCS).

1. Logige LCS-i sisse ja avage soovitud keskkond.
2. Avage **Kõik üksikasjad**.
3. Valige **Hooldamine** või kerige alla kiirkaardile **Keskkonna lisandmoodulid**.
4. Valige **Installi uus lisandmoodul**.
5. Valige **Kulude halduse teenus**.
6. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.
7. Valige **Installi**.

**Funktsioonide halduse** tööruumis lülitage sisse järgmised funktsioonid:

- Uuendatud kuluaruanded
- Kulude automaatne vastendamine ja loomine kviitungist

Nende funktsioonide sisselülitamisel ilmnevad järgmised toimingud.

- Olemasolev **Kulude halduse** tööruum asendatakse uue tööruumiga.
- Lisarud on uus menüükäsk kuluvälja nähtavuse jaoks.
- Saate siiski avada endise **Kuluaruannete** lehe, avades **Kuluhaldus > Minu kulud > Kuluaruanded**.
- Töövood ja mis tahes kinnitused viivad teid endiselt olemasolevate kuluaruannete lehele.
- Kviitungeid töödeldakse teenuse Microsoft Azure Cognitive Services kaudu ja metaandmed ekstraktitakse ning lisatakse.
- Lisati suvand, mis võimaldab teil luua kuluaruande, mis sisaldab vastendatud manustamata kviitungeid.
- Kuluaruannetele lisatav suvand võimaldab teil luua kviitungist kulurea või üritab sobitada olemasolevat kviitungit olemasoleva kulureaga.

Lisateavet kuluaruannete uuendamise funktsiooni kohta vt teemast [Kuluaruannete uuendamine](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**

Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli. See mudel ei põhine teie üleslaaditud kviitungitel.

**Kus see funktsioon on saadaval ja töödeldud?**

Praegu toetatakse Ameerika Ühendriike.

**Kuhu mu kviitungid lähevad?**

Finance võtab andmete ekstraktimiseks ühendust teenusega Cognitive Services. Teenus Cognitive Services säilitab töötlemisel teie kviitungi koopia kuni 24 tunniks. Pärast töötluse lõpetamist eemaldab teenus Cognitive Services kviitungi. Kviitungid talletatakse endiselt Finance'is.

Lisateavet vt teemast [Kviitungi mõistmise lubamine vormituvasti uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
