---
title: Osaliselt reserveeritud üleviimistellimuste hulgiväljastamine
description: See artikkel kirjeldab, kuidas seadistada ja rakendada osaliselt reserveeritud üleviimistellimuste pakkvabastust mobiilsest seadmest.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218678"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Osaliselt reserveeritud üleviimistellimuste hulgiväljastamine

[!include [banner](../includes/banner.md)]

Osaliselt reserveeritud üleviimistellimuste hulgiväljastamise funktsioon võimaldab pakett-töö abil üleviimistellimusi osaliselt lattu väljastada.
Kuna on olemas osalise koguse väljastamise võimalus, ei pea enne tellimuse väljastamist ootama, et terve tellimuse kogus laos kättesaadav oleks.

Tellimuste lattu väljalase on laohaldusprotsess (WMS). See protsess hõlmab tegevusi, nagu komplekteerimine, pakkimine ja saatmine, mida laotöötaja saab mobiilse seadme abil teha.

## <a name="where-it-applies"></a>Kus see kehtib

Selle funktsiooni puhul väljastatakse üleviimistellimused lattu pakett-töö abil. See funktsioon on abiks, kui teil pole laos piisavalt varusid, kuid soovite siiski kaupu ühest laost teise üle viia.

## <a name="how-it-is-set-up"></a>Kuidas see seadistatakse

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Määrake üleviimistellimuste ja müügitellimuste täitmise kriteeriumid

Enne, kui tellimuse saab osaliselt partiina lattu väljastada, peavad täitmise kriteeriumid olema täidetud. Need täitmise kriteeriumid määratakse täitmispoliitikaga.

Üleviimistellimuste ja müügitellimuste täitmispoliitikad määratakse ettevõtte tasandil. Olenevalt täitmispoliitika seadistusest võetakse tellimuste väljastamine partiina vastu või lükatakse tagasi. Seejärel töödeldakse tellimusi vastavalt.

- Üleviimistellimuste **\>\>\> ja müügitellimuste täitmispoliitikate loomiseks minge laohalduse häälestusprogrammi lao täitmispoliitikasse ja looge täitmispoliitika**, sisestades nime ja kirjelduse.
- Täitmismäära, väärtuse tüübi ja teate määramiseks, mis kuvatakse täitmispoliitika rikkumise korral, **\>\>\> minge laohalduse häälestuse vabastamise poliitikasse ja seadke täitmismäär** **·**, **·** **väärtuse** tüüp ja täitmise rikkumise teate väljad.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Määrake üleviimistellimuste ja müügitellimuste täitmise poliitikad

- Üleviimistellimuste täitmispoliitikate seadistamiseks minge laohalduse seadistuse varude ja laohalduse parameetritesse ja seejärel valige üleviimistellimuse täitmispoliitika jaotises Laohaldus vahekaardil Üleviimistellimused **\>\>** **.** **·**
- Müügitellimuste täitmispoliitikate seadistamiseks minge müügireskontro seadistuse müügireskontro parameetritesse ja seejärel valige laohalduse vahekaardil müügitellimuse täitmispoliitika **\>\>.** **·**

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Luba vabastus partiina ja määra kogus, mis tuleb partiina vabastada

Laost tellimuste partiina väljastamiseks kasutatakse pakett-tööd. Parameetrid, mis eristavad tellimusi, mis tuleks pakett-tööna käivitada, määratakse pakett-töös eneses.

Parameeter **Kogus** määrab, kas partiina tuleks väljastada terve kogus või füüsiliselt reserveeritud kogus. Parameeter **Luba osaliselt väljastatud tellimuste väljastamine** määrab, kas partii tellimused tuleks vastu võtta või tagasi lükata, kui nad varem osaliselt väljastati.

- Üleviimistellimuste **jaoks** **osaliselt väljastatud tellimuste** parameetrite Koguse ja Lubamise parameetreid häälestamiseks minge laohalduse lattu väljastatud üleviimistellimuste **\>\> automaatseks väljalaseks.**
- Müügitellimuste jaoks **osaliselt** **väljastatud tellimuste parameetrite** Koguse ja Lubamise parameetreid häälestamiseks minge **\>\> laohalduse müügitellimuste automaatseks väljastamiseks lattu.**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
