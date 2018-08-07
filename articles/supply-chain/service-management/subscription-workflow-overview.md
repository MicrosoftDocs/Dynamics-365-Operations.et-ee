---
title: "Kordustellimuste töövoo ülevaade"
description: "Teema annab ülevaate kordustellimuse töövoost."
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b4872c0753b54bdddf2c7778a13819726eea4a90
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

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

  



