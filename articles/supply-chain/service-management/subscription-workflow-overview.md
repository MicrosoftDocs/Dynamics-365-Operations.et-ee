---
title: Kordustellimuste töövoo ülevaade
description: See artikkel annab ülevaate kordustellimuse töövoost.
author: sorenva
ms.date: 05/07/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c112e1816d7ede80e0e30fe318d159e22ab540b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897425"
---
# <a name="subscription-workflow-overview"></a>Kordustellimuste töövoo ülevaade 

[!include [banner](../includes/banner.md)]


Olete valgustusfirma kordustellimuste haldur ja teie ettevõte pakub valgustusseadmete teenuslepinguid. Klient soovib teie ettevõttelt osta aastase kordustellimuse valgustusseadmete hooldamiseks.

## <a name="setting-up-subscriptions"></a>Kordustellimuste seadistamine

Kordustellimuste seadistamiseks tuleb kõigepealt luua kordustellimuste grupp uue teenuseleppe jaoks või kontrollida, kas selline kordustellimuste grupp on juba olemas. Kui kordustellimuste grupp on olemas, tuleb see seadistada, nii et kliendile esitatakse arve kord aastas ja müügitulusid arveldatakse aasta jooksul iga kuu. Lisateavet kordustellimuste seadistamise kohta vt teemast [Kordustellimuste gruppide seadistamine](set-up-subscription-groups.md).

Pärast kordustellimuste grupi loomist saate luua kordustellimuse. Lisateavet teenuse kordustellimuste loomise kohta vt teemast [Teenuse kordustellimuste loomine kordustellimuste grupist](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Kordustellimuste kannete loomine ja muutmine

Pärast kordustellimuse seadistamist looge kordustellimuse tasukanne esimeseks arveldusperioodiks, mis on üks aasta. Kanded on tüübiga **Tavaline**. Seega saate luua ainult selliseid kordustellimuste kandeid, mille alates ja kuni kuupäevad vastavad varem vormis **Perioodi tüübid** loodud perioodidele. Lisateavet tasukannete kohta vt teemast [Kordustellimuste tasukannete loomine](create-subscription-fee-transactions.md).

Pärast kliendile kordustellimuse seadistamist meenub teile, et oli kokku lepitud 10-protsendine allahindlus kõigist teenuspakkumiste hinnakirja hindadest. Seepärast tuleb teil vähendada loodud tasukande hinda.

Hiljem samal päeval teatab kliendi kontaktisik, et kuigi nad endiselt soovivad valgusseadmete teenuselepet, soovivad nad hiljem samal aastal paigaldada uue valgusseadme. Seega vajavad hooldusteenust kuni oktoobrini 2013. Kliendi kordustellimuses kuude arvu vähendamiseks loote uue kordustellimuste tasukande tüübiga **Vähendamispäevad**. Lisateavet päevade vähendamise kohta vt teemast [Kordustellimuste tasude päevade vähendamine](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Arve koostamine ja kordustellimuste kannete kogumine

Olete nüüd lõpetanud kordustellimuse seadistamise ja olete valmis kliendile arvet koostama. Lisateavet kordustellimuste arveldamise kohta vt teemast [Kordustellimuste kannete arveldamine](invoice-subscription-transactions.md).

Kaks päeva hiljem helistab klient, et kordustellimuse arve peaks koostama USA dollarites, mitte eurodes. Seega loote kreeditarve ja ka uue kordustellimuse kande vajalikus valuutas. Lisateavet kordustellimuste kannete krediteerimise kohta vt teemast [Kordustellimuste kannete krediteerimine](credit-subscription-transactions.md).

Iga kuu lõpus saate koguda ühe kuu tulu kliendi kordustellimuselt kasumi- ja kahjumikontole ning lõpetamata toodangu kontodele. Lisateavet kordustellimuste tulude kogumise kohta vt teemast [Kordustellimuse tulu kogumine](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]