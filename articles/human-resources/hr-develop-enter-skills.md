---
title: Sisestage oskused
description: Tööd ja haldurid saavad oskuseid sisestada rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c2a35079f43b92b5ff6d68aa7068f3e1f68ce8c2c32d23cdd22798f95c9a0ff4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732221"
---
# <a name="enter-skills"></a>Sisestage oskused

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate sisestada töötajate, kandidaatide või kontaktisikute oodatavad oskused või tegelikud oskused rakenduses Dynamics 365 Human Resources. Oodatav oskus on oskus, mille isik kavatseb omandada. Tegelik oskus on oskus, mis isikul praegu on.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Töövoo loomine oskuste automaatseks kinnitamiseks

Oskuste sisestamiseks ilma kinnitamist nõudmata peate oskuste automaatseks kinnitamiseks looma töövoo.

> [!NOTE]
> Töötajate sisestatud oskused vajavad alati juhi kinnitust. See töövoog kinnitab automaatselt ainult juhtide sisestatud oskused oma töötajate nimel.

1. Tööruumis **Personalihaldus** valige **Lingid**.

2. Jaotises **Seadistus** valige suvand **Inimressursside töövood**.

3. Valige suvand **Uus**.

4. Valige **Loo töövoog** paanil väli **Töötaja oskused**.

   [![Töötaja oskuste töövoo valimine.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. **Ava see fail?** dialoogiboksis valige **Ava**. Kui teil palutakse, sisestage oma volitused.

6. Valige töövoo redaktoris **Kinnitage oskused** töövoo element ja lohistage see lõuendile.

   [![Valige oskuste töövoo elemendi kinnitamine.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Ühendage **Alusta** element **Kinnita oskused 1** elemendiga ja seejärel ühendage **Kinnita oskused 1** element elemendiga **Lõpp**. Võimalik, et peate elemendi **Lõpp** vaatamiseks alla kerima. Saate seda lohistada teiste elementideni lähemal.

   [![Ühendage töövoo elemendid.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Topeltklõpsake **1Kinnita oskused 1** töövoo element ja paremklõpsake **Samm 1** element. Paremklõpsake **Samm 1** element ja valige suvand **Atribuudid**.

9. **Atribuutide** aknas valige **Tingimus** vasakpoolsel navigeerimisribal.

10. Valige suvand **Käivita see samm üksnes siis, kui järgmine tingimus on täidetud**.

11. Valige **Lisa tingimus**. Pärast **Kus** käsku valige **Töötaja iseteenindusoskused** ja seejärel valige **Töötaja iseteenindusoskused. Isik**. Pärast **on** valige **väli** ja seejärel valige **Kasutaja suhe isikuga. Isik**.

    [![Määra tingimus.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Valige **Määrang** vasaku käe navigeerimisribal.

13. Vahekaardil **Määrangu tüüp** valige **Hierarhia**.

14. Valige **Hierarhia valik** vahekaardil **Hierarhia tüüp:** väärtus **Juhtimishierarhia**.

    [![Määrake juhtimishierarhia.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Valige **Sule** ja seejärel valige **Töövoog** lõuendi tööreas, siis valige **Salvesta ja sule**.

Lisateavet töövoogudega töötamise kohta vt teemast [Töövoosüsteemi ülevaade](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Sisestage töötaja oskused

1. Vali töötaja.

2. Valige **Töötaja** lehel tegevusribalt **Isik** ja seejärel **Oskused**.

3. Täitke **Oskused** lehel iga oskuse jaoks järgmised väljad:

   - **Oskus**: Valige oskus.
   - **Taseme tüüp**: Valige **Tegelik** oskus töötaja olemaoslevale oskusele või **Soovitud** oskus töötaja oskuse jaoks, mida ta sihib.
   - **Tase**: Valige töötaja oskuse tase.
   - **Taseme kuupäev**: Valimiseks klõpsake kalendris kuupäeva.
   - **Kontrollija**: Vajadusel valige loendist soovitud kontrollija. Saate otsingut filtreerida.
   - **Kogemuse aasta**: Sisestage kogemuse aasta.
   - **Kinnitatud**: Kui oskus on kinnitatud, märkige ruut.
   - **Kinnitaja**: Sisestage kinnitaja nimi.

4. Kui olete oskuste sisestamise lõpetanud, valige **Salvesta**.

## <a name="see-also"></a>Vt ka

[Oskuste konfigureerimine](hr-develop-skills.md)<br>
[Oskuste kaardimine](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]