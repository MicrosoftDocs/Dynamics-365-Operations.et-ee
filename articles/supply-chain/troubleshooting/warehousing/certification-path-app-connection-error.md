---
title: Sertifikaadi tee tõrge rakenduse ühenduse seadistamisel
description: Kui Warehouse Management rakendus näitab tõrget "Usaldusankrut sertifikaadi tee jaoks ei leitud", kasutage seda lehte probleemi lahendamiseks.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476123"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Sertifikaadi tee usaldusankrut ei leitud rakenduse ühenduse häälestamisel

## <a name="symptoms"></a>Sümptomid

Kui proovite luua ühendust rakendusega Supply Chain Management, võib Warehouse Management rakendus teile kuvada järgmise tõrketeate:

> java.security.cert.certPathValidatorException: usaldusankru sertifitseerimise teed ei leitud.

See probleem võib mõjutada järgmiste atribuutidega seadmeid:

- **Operatsioonisüsteemi versioon**: Android 4.4.x (nagu näiteks Zebra TC55). Seda probleemi pole viimastes Android versioonides.
- **Supply Chain Management asukoht**: Pilves
- **Ühendusrežiim**: kliendi saladus või sert

## <a name="possible-cause"></a>Võimalik põhjus

Microsoft võib olla värskendanud serveri SSL-i serte, mida kasutab rakendus Supply Chain Management. Seetõttu võib juursertifikaat ja/või üks vahesertifikaatidest olla muutunud, nii et uus sert ei ole mobiilse seadme usaldusväärsete süsteemisertifikaatide loendis. Uuemad Android versioonid uuendavad automaatselt usaldusväärseid sertifikaate, kuid Android 4.4.x mitte.

## <a name="resolution"></a>Lahendus

Proovige teha probleemi lahendamiseks järgmist:

- Kasutage järgmises jaotises kirjeldatud lahendust iga vastava seadme värskendamiseks.
- Võib olla *võimalik* võtta ühendust Zebra või Google`iga et uuendada usaldusväärse sertifitseerimisasutuse (CA) serte. Kuid me ei ole seda kinnitanud.
- Võimaluse korral kaaluge vanemate seadmete asendamist seadmetega, mis töötavad uuema Android versiooniga (kus usaldusväärsed CA-tunnistused uuendatakse automaatselt).

### <a name="workaround"></a>Vastukaal

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>1. etapp: eksportige uus juursert rakenddusest Supply Chain Management

Laadige uus juursert käsitsi alla oma Interneti-brauseri abil, tehes järgmist:

1. Logige sisse Dynamics Supply Chain Management ja avage esileht.

1. Brauseri aadressiribal valige luku ikoon, et avada **asukoht on turvaline** dialoogiaken.
1. Dialoogiaknas valige **Sert (kehtiv)** et avada **serdi** aken selle sertifikaadi jaoks.
1. Avage **serdi tee** vahekaart **serdi** aknas.
1. Valige hierarhias näidatud ülemine sertifikaat. (see on juursertifikaat).
1. Avage **Üksikasjad** vahekaart **serdi** aknas.
1. Valige **Kopeeri fail** nupp **Üksikasjad** vahekaardi all.
1. Avaneb **Sertifikaadi ekspordiviisard**. Jätkamiseks valige nupp **Edasi**.
1. Avaneb **ekspordifaili vormingu** leht. Valige **DER-kodeeritud kahendfail X.509 (.CER)**. Jätkamiseks valige nupp **Edasi**.
1. Avaneb **eksporditav fail** leht, kus määrake faili nimi ja asukoht. Jätkamiseks valige nupp **Edasi**.
1. Avaneb **sertifikaadi ekspordiviisardi lõpuleviimine** leht, mis näitab teie ekspordi tulemust. Valige **Lõpeta**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>2. etapp: installige allalaaditud sert mõjutatud seadmetele

Installige allalaaditud tunnistus järgmiselt:

1. Kandke eelmises sammus allalaaditud sert üle seadmesse, mida soovite värskendada. Te võite näiteks kasutada SD-kaarti või võrguühendust, et teha fail oma seadmes kättesaadavaks.
1. Avage oma seadme turvasätted ja valige menüü suvand serdi installimiseks failist. (Täpsed sammud selle jaoks erinevad seadme ja operatsioonisüsteemi versiooni alusel.)
1. Uus sert tuleks nüüd usaldusväärsete sertifikaatide jaoks **kasutaja** vahekaardil kuvada.
1. Korrake seda toimingut iga asjakohase toote puhul.
