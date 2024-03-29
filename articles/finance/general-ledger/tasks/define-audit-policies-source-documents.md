---
title: Lähtedokumentide jaoks auditipoliitikate määratlemine
description: See artikkel selgitab, kuidas auditi poliitika reegleid seadistada ja käivitada.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8aa106cd5a5596f6b9a6663390e03ebc3f91a7b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872524"
---
# <a name="define-audit-policies-for-source-documents"></a>Lähtedokumentide jaoks auditipoliitikate määratlemine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas auditi poliitika reegleid seadistada ja käivitada. Näites kasutatakse hotelli kulu tüübiga kuluaruandeid. See protsess kasutab demoettevõtte USMF-i andmeid. Audiitori roll sisaldab nende ülesannete teostamiseks vajalikke õigusi.

1. Navigeerimispaanil avage **Moodulid > Auditi töölaud > Seadistus > Poliitika reegli tüüp**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Reegli nimi**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Väljal **Päringu nimi** valige **Kuluaruande rida**.
6. Väljal **Päringu tüüp** valige **Liitväärtus**.
7. Väljal **Juriidiline isik** valige **Juriidiline isik**.
8. Väljal **Dokumendi kuupäeva viide** valige **Muutmise kuupäev ja kellaaeg**
9. Valige käsk **Salvesta**.
10. Navigeerimispaanil avage **Moodulid > Auditi töölaud > Seadistus > Auditipoliitika**.
11. Valige suvand **Uus**.
12. Sisestage väärtus väljale **Nimi**.
13. Laiendage jaotist **Poliitika organisatsioonid**.
14. Puus valige **Contoso Meelelahutussüsteem USA**, seejärel valige **Lisa**.
15. Puus valige **Contoso Nõustamine USA**, seejärel valige **Lisa**.
16. Puus valige **Contoso Jaemüük USA**, seejärel valige **Lisa**.
17. Ahendage jaotist **Poliitika organisatsioonid**.
18. Laiendage jaotist **Poliitika reeglid**.
19. Leidke ja valige loendist varem loodud poliitika reegel.
20. Valige **Poliitika reegli loomine**.
21. Sisestage kuupäev ja kellaaeg väljale **Jõustumiskuupäev**.
22. Valige **Filter**.
23. Loendist valige rida **Kulukategooria** ja seadke üksikasjad valikule **Hotell**.
24. Sisestage või valige väärtus väljal **Kriteeriumid**.
25. Valige vahekaart **Liitväärtus**.
26. Valige **Lisa**.
27. Loendist valige välja väärtus **Kandesumma**.
28. Väljale **Väli** sisestage või valige väärtus.
29. Väljal **Liitväärtuse funktsioon** valige **Summa**.
30. Valige vahekaart **Grupeerimisalus**.
31. Valige **Lisa**.
32. Loendist valige välja väärtus **Töötaja**.
33. Valige **Lisa**.
34. Loendist valige välja väärtus **Kulukategooria**.
35. Väljale **Väli** sisestage või valige väärtus.
36. Valige vahekaart **Saamine**.
37. Valige **Lisa**.
38. Valige **Kandesumma**.
39. Väljale **Väli** sisestage või valige väärtus.
40. Väljal **Liitväärtuse funktsioon** valige **Summa**.
41. Väljale **Kriteerium** sisestage `>2000`.
42. Valige nupp **OK**.
43. Valige **Test**.
44. Väljale **Dokumendi valimise alguskuupäev** sisestage kuupäev ja kellaaeg.
45. Väljale **Dokumendi valimise lõppkuupäev** sisestage kuupäev ja kellaaeg.
46. Valige **Käivita test**.
47. Toimingupaanil valige **Auditipoliitika**.
48. Valige **Lisasuvandid**.
49. Väljale **Alguskuupäev** sisestage kuupäev ja kellaaeg.
50. Väljale **Lõppkuupäev** sisestage kuupäev ja kellaaeg.
51. Valige **Partii**.
52. Laiendage jaotist **Käivita taustal**.
53. Valige väärtus **Jah** väljal **Pakett-töötlus**.
54. Valige nupp **OK**.
55. Navigeerimispaanil avage **Moodulid > Auditi töölaud > Auditi juhtumid**.
56. Otsige loendist ja valige soovitud kirje.
57. Laiendage jaotist **Seosed**.
58. Otsige loendist ja valige soovitud kirje.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
