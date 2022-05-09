---
title: Maksukoodi ei saa määrata.
description: See teema kirjeldab, kuidas sooritada maksuarvestuse teenuses tõrke "Maksukoodi ei saa määrata" tõrkeotsingut.
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
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648139"
---
# <a name="tax-code-cannot-be-determined"></a>Maksukoodi ei saa määrata.

[!include [banner](../includes/banner.md)]

See teema selgitab tõrkeotsingu etappe, mida saate maksu arvutamise teenuses tõrke "Maksukoodi ei saa määrata" korral ette võtta.

## <a name="symptom"></a>Sümptom

Saate järgmise tõrketeate: "Päis/read - 1, maksukoodi ei saa määrata." Teise võimalusena leiate vea tõrkeotsingu failist, nagu näha järgmises näites. Lisateabe saamiseks vt luba silumisrežiim [tõrkeotsinguks](tcs-troubleshooting-enable-debug-mode.md).

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

Probleem toimub tõenäoliselt seetõttu, et maksugrupp ja kauba maksugrupp ei ristu.

## <a name="troubleshoot"></a>Tõrkeotsing

Järgige neid samme probleemi tõrkeotsinguks.

1. Kontrollige tõrkeotsingu failis, kas maksugrupp ja kauba käibemaksugrupp on määratletud. Kui maksugrupi ja **kauba** maksugrupi **väärtused** on tühjad, pole maksugruppi ja kauba käibemaksugruppi määratletud. Kui need on määratletud, võivad tulemused olla valed.

    Siin on tõrkeotsingu faili näide.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. Kontrollige **, et käibemaksu alistamise** suvand vahekaardil **Seadistus** müügitellimuse rea üksikasjades on lubatud.

    - Kui see on lubatud, määravad maksukoodid **maksugrupp** **ja kauba maksugrupi** väärtused, mille kandereale sisestate. Kontrollige, kas need väärtused on õigesti sisestatud.
    - Kui see ei ole lubatud, kontrollige **·** **, et maksugrupi kohaldatavus ja kauba maksugrupi kohaldatavusväljadele on määratud õiged** väärtused. Lisateavet vt jaotisest Ei [leitud vastavaid tulemusi](tcs-troubleshooting-no-matching-result.md).

3. Kui maksugrupp ja kauba käibemaksugrupp on korrektselt määratletud, määratlege, kas nende puhul on olemas mis tahes ristvalikud.

    1. Minge RCS-i maksufunktsioonid **Maksukoodid** \> **ja -grupid Maksugruppi.** \> **·**

        | Rea maksugrupp | Maksukoodid |
        |----------------|-----------|
        | Grupp A        | A         |

    2. Minge maksufunktsioonid **Maksukoodid** \> **ja -grupid** \> **Kauba käibemaksugrupp.**

        | Rida. Kauba maksugrupp | Maksukoodid |
        |---------------------|-----------|
        | Grupp B             | B         |

    Kui maksugrupi ja kauba maksugrupi puhul pole ühtegi ristsektsiooni, siis maksukoodi ei määratleta.

## <a name="mitigation"></a>Vähendamine

1. Läbige selle teema tõrkeotsingu [jaotises](#troubleshoot) kõik etapid ja parandage seadistus vastavalt vajadusele. Kui maksugrupp ja kauba käibemaksugrupp pole õigesti määratletud, [vt ühtivad tulemused puuduvad](tcs-troubleshooting-no-matching-result.md).
2. Kui maksugrupi ja kauba maksugrupi kohta pole ühtegi ristsektsiooni, looge RCS-is uus funktsiooniversioon ja parandage seadistus.

    - Minge **maksufunktsioonid** \> **Maksukoodid ja groupsItem** > **maksugrupp.**

        | Rida. Kauba maksugrupp | Maksukoodid |
        |---------------------|-----------|
        | Grupp B             | A; B       |

    Maksukood määratletakse A-ga **·**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
