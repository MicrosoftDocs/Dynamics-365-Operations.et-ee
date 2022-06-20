---
title: Vastavaid tulemusi ei leitud
description: See artikkel selgitab, kuidas teha maksuarvutuse teenuses tõrke "Vastavat tulemust ei leita" tõrkeotsingut.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845140"
---
# <a name="no-matching-result-could-be-found"></a>Vastavaid tulemusi ei leitud

[!include [banner](../includes/banner.md)]

See artikkel selgitab tõrkeotsingu samme, mida võite ette võtta, kui saate maksu arvutamise teenuses tõrke "Vastavustulemust ei leitud".

## <a name="symptom"></a>Sümptom

Saate järgmise tõrketeate: "Päis/read - 1, maksugrupp, vastavat tulemust ei leitud."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Põhjus

Probleem ilmneb, kui regulatiivse konfiguratsiooniteenuse (RCS) funktsiooniseadistus on vale.

## <a name="troubleshoot"></a>Tõrkeotsing

1. Laadige alla tõrkeotsingu fail. Lisateabe saamiseks vt luba silumisrežiim [tõrkeotsinguks](tcs-troubleshooting-enable-debug-mode.md).
2. Võrrelge maksuteenuse arvutuse sisendit häälestuse probleemi lahendamiseks funktsiooniseadistusega.

    Järgmine näide näitab maksuteenuse arvutuse sisendit.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Järgmises tabelis loetletakse maksugrupi kohaldatavus RCS-s.

    | Header.Businessi protsess | Read.Äriüksus | Header.Ship sihtnumbrist | Maksugrupp |
    |-------------------------|---------------------|---------------------------|-----------|
    | Tööleht                 |                     |                           | Grupp A   |
    | Müük                   |                     | 30160                     | Grupp B   |

    Maksuteenuse arvutuse sisendi **kohaselt on** **·** **äriprotsessi** **väärtus päisel Müük ja päises oleva sihtnumbri lähetusväärtus 30159.** See sisend põhineb RCS-i kohaldatavusreeglite seadistusel. Kuna ühtivad jooned puuduvad, ilmneb tõrge.

    > [!NOTE]
    > Kui kohaldatavusreegli väärtus on tühi, kehtib reegel mis tahes väärtusele.

## <a name="mitigation"></a>Vähendamine

Tõrke vähendamiseks järgige neid juhiseid.

1. RCS-s minge **globaliseerimisfunktsiooni** \> **maksuarvutusse**.
2. Saate luua funktsiooni uue versiooni.
3. Lisage rida vastava teabe jaoks.

    | Header.Businessi protsess | Read.Äriüksus | Header.Ship sihtnumbrist| Maksugrupp |
    |-------------------------|---------------------|--------------------------|-----------|
    | Tööleht                 |                     |                          | Grupp A   |
    | Müük                   |                     | 30160                    | Grupp B   |
    | Müük                   |                     | 30159                    | Grupp B   |

4. Avaldage funktsiooni häälestuse versioon.
5. Finantsis Microsoft Dynamics 365 minge maksu **seadistamise** \> **maksu** \> **konfiguratsiooni** \> **maksu arvutamise parameetritesse** ja valige uus versioon.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
