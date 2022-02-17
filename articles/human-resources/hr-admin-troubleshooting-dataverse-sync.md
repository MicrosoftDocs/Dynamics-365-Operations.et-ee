---
title: Dataverse sünkroonimise lähtestamine
description: See teema kirjeldab, kuidas teha nende kirjete tõrkeotsingut, mis ei ole Microsoft Dynamics 365 Human Resources ja inimkapitali halduse (HCM) ühise lahenduse vahel õigesti Microsoft Dataverse sünkroonitud.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d6b20b6b2ae4fdbbfb27a765dfb7a1dc82fe7981
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071156"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse sünkroonimise lähtestamine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Probleem

Microsoft Dynamics 365 Human Resources ja inimressursside halduse (HCM) ühise lahenduse üksuste vahel pole kirjeid Microsoft Dataverse sünkroonitud. Sünkroonimise kohta lisateabe saamiseks minge [Dataverse integratsiooni konfigureerimine](hr-admin-integration-common-data-service.md). Õige sünkroonimise ebaõnnestumine võib ilmneda siis, kui **Dataverse integratsiooni uuesti proovimise** või **Dataverse integratsiooni vastamata päringute sünkroonimise** partii tööd on olekus **Täitmine**.

## <a name="resolution"></a>Lahendus

Kui **Dataverse integreerimise uuesti proovimise** või **Dataverse integratsiooni vastamata taotluse sünkroonimise** partii tööd on olekus **Täitmine** või **Tühistamine**, saate oleku lähtestada. Seda saab teha, tühistades partii töö, järgides juhendit [Lähtesta kinnised partii tööd](hr-admin-troubleshooting-batch-execution.md). Pärast partii töö tühistamist saate selle lähtestada, seadistades selle olekusse **Ootel**. Seejärel käivitatakse partii töö järgmise planeeritud käitusaja jooksul.

1. Kui te pole seda juba teinud, lubage funktsioon **Täiustatud partii katkestamise** **Funktsioonihalduses**.
   1. Minge **Funktsioonihalduse** lehele (**Süsteemihaldus** > **Kokkuvõte** > **Funktsioonihaldus**).
   2. Valige vahekaart **Kõik**.
   3. Valige veerg **Funktsiooni nimi** ja filtreerige **Täiustatud partii katkestamise** abil.
   4. Valige **Lubage** tegevus, kui see pole veel lubatud.

2. Lülitage Dataverse integratsioon välja.
   1. Minge **Microsoft Dataverse integratsiooni** lehele (**Süsteemihaldus** sealt minge **Lingid** > **Integratsioonid** > **Dataversekonfiguratsiooni**).
   2. Määrake suvand **Luba Dataverse integratsioon** valikule **Ei**.

3. Tühistage **Dataverse integratsiooni uuesti kordamise** partii töö.
   1. Minge lehele **Partii tööd** (**Süsteemihaldus** minge  **Lingid** > **Partii tööd** > **Partii tööd**).
   2. Filtreerige **Töö kirjelduse** veerg **Integratsiooni** alusel.
   3. Valige **Dataverse integratsiooni uuesti kordamise** partii töö.
   4. Tegevuse lindil valige **Partii töö**, **Sundtühistamine** ja seejärel valige kinnitamiseks **Jah**.

   > [!NOTE]
   > Sõltuvalt sellest, millal integratsioon esimest korda lubati, võib partii tööl olla kirjelduse **Common Data Service integratsiooni uus katse**. Valige see partii töö, kui see on loetletud, mitte **Dataverse integratsiooni uue katse** partii tööna.

4. Kustutage kõik Dataverse integratsiooni partii tööd.
   1. Valige **Partii tööde** lehel **Dataverse integratsiooni vahele jäänud taotluse sünkroonimine**, **Dataverse integratsiooni uuesti käivitamine** ja **Dataverse integratsiooni algse sünkroonimise** partii tööd.
   2. Tegevuse lindil valige tegevus **Muuda olekut**. 
   3. Valige **Peata** ning seejärel **OK**.
   4. Tegevuse lindil valige **Kustuta** tegevus ja seejärel valige tegevuse kinnitamiseks **Jah**.

5. Lülitage sisse Dataverse integratsiooni partii tööd.
   1. Minge **Microsoft Dataverse integratsiooni** lehele (**Süsteemihaldus** > **Lingid** > **Integratsioon** > **Dataverse konfiguratsioon**).
   2. Määrake suvand **Luba Dataverse integratsioon** valikule **Jah**.

6. Minge **Partii tööde** lehele ja kinnitage, et **Dataverse integratsiooni korduses** ja **Dataverse integratsioonis vahele jäänud taotlusega** sünkroonimise partii tööd on loodud.

Partii tööde taasloomise abil saate nüüd jälgida **Dataverse integratsiooni kordamise** partii tööd, et näha, kui kaua selle töö tegemine kestab. Siis saate kontrollida, kas kirjed sünkroonitakse õigesti Microsoft Dataverse HCM-i üldise lahendusega.

## <a name="see-also"></a>Vt ka

[Dataverse’i integratsiooni konfigureerimine](hr-admin-integration-common-data-service.md)<br>
[Kinni jäänud pakett-tööde lähtestamine](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
