---
title: Viitvõla sisestusmeetodid
description: See artikkel kirjeldab erinevusi viitvõla sisestusmeetodite vahel tulude ja kulude viitvõlgade osas kordustellimuse arvelduses.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017473"
---
# <a name="deferral-posting-methods"></a>Viitvõla sisestusmeetodid

See artikkel kirjeldab erinevusi viitvõla sisestusmeetodite vahel tulude ja kulude viitvõlgade osas kordustellimuse arvelduses.

Tulude ja **kulude viitvõla parameetrite lehel** **on viitvõla sisestusmeetodite valikud Bilanss ning** **Tulu ja kulu**. Selles artikli näites seletatakse kahe meetodi vahelisi erinevusi ja põhjusi, miks te võite kasutada üht meetodit või muud.

Bilansimeetodis **kasutatakse** ainult kahte kontot. Seetõttu kaasatakse vähem seadistust. Tulu **ja kulu meetodil** on kaks lisakontot: **algne** tunnustus **ja** tunnustuse vastaskonto, sõltuvalt kande tüübist, tulu, allahindlused ja kulud. Need kontod seadistatakse viitvõlgade vaikelehel **(** Kordustellimuse arveldustulu **ja kulu viitvõlgade \> seadistus \>).** Ehkki näide keskendub viittulule, saab sama kontseptsiooni rakendada edasilükatud allahindlustele ja edasilükatud kuludele.

## <a name="example"></a>Näide

Müügiarvel 1 on kogusumma $3,000 omab viittulu. Järgmised tabelid näitavad jaotusi, kui see müügiarve on sisestatud.

**Bilansimeetod**

| Tüüp | Konto | Deebet | Krediit|
|---|---|---|---|
| Deebet | Müügireskontro | 3,000.00 | |
| Krediit | Edasilükatud tulu | | 3,000.00 |

**Kasumi ja kahjumi meetod**

| Tüüp | Konto | Deebet | Krediit |
|---|---|---|---|
| Deebet | Müügireskontro | 3,000.00 | |
| Deebet | Tulu tuvastamise vastaskonto | 3,000.00 | |
| Krediit | Edasilükatud tulu | | 3,000.00 |
| Krediit | Algne tulu tuvastamine | | 3,000.00 |

Müügiarvel 2 on kogusumma $2,000 ja sellel ei ole edasilükatud tulu.

| Tüüp | Konto | Summa |
|---|---|---|
| Deebet | Müügireskontro | 3,000.00 |
| Krediit | Tulu | 3,000.00 |

**Müügiarve 1 ja 2 bilansimeetodi kogusummad ühendatud**

| Konto | Deebet | Krediit |
|---|---|---|
| Müügireskontro | 5,000.00 | |
| Tulu | | 2000,00 |
| Edasilükatud tulu | | 3,000.00 |

**Bilansimeetodi** kasutamisel ei ole perioodi brutotulu näha nii lihtne. Osa tulust sisestatakse viittulu **kontole**. Pidage silmas, et kuna tulu tuvastatakse igas perioodis, on viittulu kontol **mitu deebeti ja kreediti**. Antud perioodi kogutulu ja tulu tuvastamise sisse-/väljaminekud segatakse.

**Müügiarve 1 ja 2 kasumi- ja kahjumimeetodi kogusummad kokku**

| Konto | Deebet | Krediit |
|---|---|---|
| Müügireskontro | 5,000.00 | |
| Tulu | | 5,000.00 |
| Tulu vastaskonto | 3,000.00 | |
| Edasilükatud tulu | | 3,000.00 |

Kogu tulu läheb tulu ja kulu **kontole**. Seejärel teisaldatakse viittulu kasumiaruandest bilansilehele. Saate hõlpsasti vaadata kogutulu, sest tulukontole sisestatakse **kõik**. Osa sellest brutotulust on siiski edasi lükatud. Seetõttu teisaldatakse see edasilükatud tulu kontole **ja** tuvastatakse hiljem.

Tulu ja **kulu meetodis** saate vaadata tulukontot ja tulu vastaskontot, **·** **et** vaadata $5,000 tulu ja netotulu (viittulu) $2,000. Kuigi kasumi **ja kahjumi meetod** võib muuta aruandluse lihtsamaks, on seadistatud rohkem kontosid.
