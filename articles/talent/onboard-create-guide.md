---
title: 'Sisseelamisjuhendi loomine ja saatmine, kasutades Dynamics 365 Talent: Onboard'
description: 'Selles teemas selgitatakse, kuidas kasutada rakendust Microsoft Dynamics 365 Talent: Onboard, et luua uutele töötajatele sisseelamisjuhend. See ülesanne on oluline esimene samm personalijuhtimise personalistrateegias.'
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4dbfcc3b3fd611eea36109a516a7b9361a9f654
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009850"
---
# <a name="create-and-send-an-onboarding-guide"></a>Sisseelamisjuhendi loomine ja saatmine

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboardis saate luua enda loodud mallidest sisseelamisjuhedeid, mis on saadaval galeriis või nullist.

Kui olete loonud sisseelamisjuhendi, saate selle saata uuele töötajale. Teise võimalusena saate saata selle mitmele uuele töötajale, mille määrate Microsoft Excel failis, mille saab alla laadida Onboardi rakendusest.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Looge sisseelamisjuhend mallist ja saatke see ühele uuele töötajale

1. Valige vasakpoolses menüüs **Mallid**.
2. Valige jaotises **Minu mallid** mall, mida soovite seadistada uue töötaja sisseelamisjuhendi jaoks.
3. Redigeerige malli, kui soovite. Ärge unustage oma tööd regulaarselt salvestada.
4. Kui olete malli redigeerimise lõpetanud, valige käsk **Loo juhend.**

    [![Sisseelamisjuhendi loomine malli põhjal](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. Sisestage akna **Loo juhend** jaotisesesse **Kes on sisse elamas** uue töötaja nimi või meiliaadress. Kui uus töötaja pole veel süsteemis olemas, valige käsk **Lisa kohe** ja sisestage töötaja teave.

    ![[Sisseelamisjuhendisse teabe sisestamine](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Valige jaotises **Millal nad alustavad** alguskuupäev.
7. Kui juhend tuleks saata automaatselt uuele tööle kindlal kuupäeval, veenduge, et **Automaatse saatmiskuupäeva ajastamine** on sisse lülitatud ja seejärel valige automaatne saatmiskuupäev. Juhendi koheseks saatmiseks lülitage välja valik **Automaatse saatmiskuupäeva ajastamine**.
8. Valige suvand **Valmis**.
9. Kui olete sisseelamisjuhendi redigeerimise lõpetanud, valige ülemises parempoolses nurgas käsk **Saada**. Seejärel järgige üht neist sammudest.

    - Uuele töötajale lingi saatmiseks valige **Kopeeri link** ja seejärel valige **Kopeeri**.
    - Sisseelamisjuhendi meili kohandamiseks enne selle saatmist valige **Meili kohandamine enne saatmist**, valige **Edasi**, kohandage meili nii, nagu soovite ja seejärel valige **Saada**.
    - Meili saatmiseks seda kohandamata valige **Edasi** ja seejärel valige **Saada**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Looge sisseelamisjuhend mallist ja saatke see mitmele uuele töötajale

Onboardis saate saata sisseelamisjuhendi mitmele uuele töötajale samal ajal.

1. Valige vasakpoolses menüüs **Mallid**.
2. Valige jaotises **Minu mallid** mall, mida soovite seadistada uute töötajate sisseelamisjuhendi jaoks.
3. Redigeerige malli, kui soovite. Ärge unustage oma tööd regulaarselt salvestada.
4. Kui olete malli redigeerimise lõpetanud, valige käsk **Loo juhend.**
5. Aknas **Loo juhend** valige **Sisseelamist vajab mitu inimest korraga**.

    [![Mitmele uuele töötajale sisseelamisjuhendi loomine](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Valige **Uue töötaja mall**.
7. Pärast xlsx-faili allalaadimist valige **Ava**, sisestage töötajate teave Exceli töövihikusse ja salvestage töövihik.

    [![Exceli malli allalaadimine, et saata sisseelamisjuhend mitmele uuele töötajale](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Enne kui saate töövihikut redigeerida, peate valima suvandi **Luba redigeerimine** Excelis.
    > 
    > [![Redigeerimise lubamine](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Lohistage Exceli töövihik määratud alale aknas **Mitme juhendi loomine** või klõpsake sellel alal suvalist kohta, et sirvida faili oma arvutis.

    [![Redigeeritud töövihiku lohistamine](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Kui olete sisseelamisjuhendi redigeerimise lõpetanud, valige ülemises parempoolses nurgas käsk **Saada**. Seejärel järgige üht neist sammudest.

    - Uutele töötajatele lingi saatmiseks valige **Kopeeri link** ja seejärel valige **Kopeeri**.
    - Sisseelamisjuhendi meili kohandamiseks enne selle saatmist valige **Meili kohandamine enne saatmist**, valige **Edasi**, kohandage meili nii, nagu soovite ja seejärel valige **Saada**.
    - Meili saatmiseks seda kohandamata valige **Edasi** ja seejärel valige **Saada**.

## <a name="create-a-guide-without-using-a-template"></a>Looge juhend malli kasutamata

Te ei pea alati mallist juhendit looma. Soovi korral saate selle asemel luua juhise nullist.

1. Vasakul menüüs valige **Juhendid** ja seejärel valige nupp **Lisa** (plussmärk \[**+**\]).
2. Sisestage akna **Loo juhend** jaotisesesse **Kes on sisse elamas** uue töötaja nimi või meiliaadress. Kui uus töötaja pole veel süsteemis olemas, valige käsk **Lisa kohe** ja sisestage töötaja teave.

    ![[Sisseelamisjuhendisse teabe sisestamine](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Valige jaotises **Millal nad alustavad** alguskuupäev.
4. Kui juhend tuleks saata automaatselt uuele tööle kindlal kuupäeval, veenduge, et **Automaatse saatmiskuupäeva ajastamine** on sisse lülitatud ja seejärel valige automaatne saatmiskuupäev. Juhendi koheseks saatmiseks lülitage välja valik **Automaatse saatmiskuupäeva ajastamine**.
5. Valige suvand **Valmis**.

## <a name="save-a-guide-as-a-template"></a>Saate salvestada juhendi mallina

Saate salvestada sisseeleamisjuhendi mallina. Sel viisil saate säästa aega, kui peate hiljem rohkem juhendeid looma.

1. Valige vasakpoolses menüüs **Juhendid**.
2. Valige nupp **Veel** (kolmikpunkt \[**...**\]) juhendile, millest soovite malli luua, ja seejärel valige **Salvesta mallina**.

    ![[Sisseelamisjuhendi salvestamine mallina](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Sisestage aknas **Salvesta uue mallina** uue malli nimi ja seejärel valige **Salvesta**.

## <a name="next-steps"></a>Järgmised etapid

- [Sisseelamisjuhendite ja mallide redigeerimine](./onboard-edit-guides-templates.md)
- [Sisu jagamine teiste kaasautoritega](./onboard-share-template.md)
- [Vaadake tööülesannete ja töötajate töölevõtmise olekut](./onboard-view-status.md)
- [Looge Onboardis värbamismeeskonnad](./onboard-create-team.md)

### <a name="see-also"></a>Vt ka

- [Proovige või ostke Onboardi rakendus](https://dynamics.microsoft.com/talent/onboard/)
- [Mis on uut?](./whats-new.md)
- [Väljalaskemärkmed](https://docs.microsoft.com/business-applications-release-notes/index)
- [Toe hankimine](./talent-support.md)
