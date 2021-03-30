---
title: Hinnasimulatsioon
description: Selles artiklis antakse teavet pakkumiste hinnasimulatsiooni kohta. Hinnasimulatsiooni abil saate hinnata mahaarvamiste mõju tulevasele müügihinale pakkumise protsessi ajal, enne kui määrate kindla hinna.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation, SalesQuotationsTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8633d6eec788035997c52322c3268b946fb0bfe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218389"
---
# <a name="price-simulation"></a>Hinnasimulatsioon

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet pakkumiste hinnasimulatsiooni kohta. Hinnasimulatsiooni abil saate hinnata mahaarvamiste mõju tulevasele müügihinale pakkumise protsessi ajal, enne kui määrate kindla hinna.

Pakkumise hinnasimulatsioon näitab uut koondsummat, mis põhineb uuel soovituslikul hinnal. Hinnasimulatsioon võib kuvada ka olemasoleva pakkumise konkreetse rea uue summa. Saate sisestada hinnasimulatsiooni ja selle hiljem rakendada. Teise võimalusena võite kasutada esialgset pakkumist ilma hinnasimulatsioonita ja teha veel muudatusi, kui koos kliendiga müügiprotsessis edasi liigute.  

Hinnasimulatsioon ei muuda pakkumise hinda. Hinnasimulatsiooni rakendamisel kogu pakkumisele käsitletakse seda pakkumise päises spetsiaalse allahindlusena. Hinnasimulatsiooni rakendamisel konkreetsetele kaupadele käsitletakse seda pakkumise ridadel spetsiaalse allahindlusena. Hinnasimulatsiooni rakendamisel ühiku müügihind loodud pakkumise real ei muutu. Selle asemel rakendatakse allahindluse protsenti, mis vastab hinna pakkumise rea hinna vähendamisele. Kui rakendatakse hinnasimulatsiooni, kantakse ühiku müügihind ja allahindluse protsent pakkumise reale või pakkumise päisesse.  

>[Märkus.] Hinnasimulatsiooni käigus kasutatakse simulatsiooni loomiseks ainult praegust müügivaluutat. Kui vaatate pakkumiste kokkuvõtteid, näete siiski ettevõtte valuuta ja müügivaluuta kombinatsiooni.  

Pakkumise ridadele lisatavad lisakaubad võivad põhjustada rea allahindlusi või multiallahindlusi. Need võivad käivitada ka koondallahindlusi, mis muudavad pakkumise ridade brutokasumit ja kasumiprotsente ning kogu allahindlust.  

Saate käitada mitut hinnasimulatsiooni, et jälgida hinnakohanduste toimeid pakkumise sihtmärkidele. Selliste simulatsioonide käitamine võimaldab teil kohandada pakkumise kogu hinda või pakkumise ühe või mitme kindla rea hinda ning seejärel rakendada hinnasimulatsiooni, mis aitab kõige suurema tõenäosusega müügitehingu sõlmida.  

Pakkumise loomisel saate seadistada märguande. Siin on mõned märguannete kasutamise viisid.

-   Need võivad hoida teid kursis pakkumiste olekuga organisatsioonis.
-   Need võivad käivitada kindla pakkumise ülevaatamise või anda teada, millal allahindluse limiite ületatakse.

## <a name="price-simulation-and-discounts"></a>Hinnasimulatsioon ja allahindlused
Et tagada allahindluste ja hindade õige arvestamine, olge allahindlusega pakkumiste hinnasimulatsioonide tegemisel väga ettevaatlik. Kuna kõiki hinnasimulatsioone käsitletakse spetsiaalsete allahindlustena aktiivsel pakkumise real või kogu pakkumisel, tuleb jälgida allahindluste erinevusi.

### <a name="types-of-discounts-in-trade-agreements"></a>Allahindluste tüübid kaubanduslepetes

Kaubanduslepped Tarneahela haldamises hõlmavad nelja allahindluse tüüpi. Neid allahindlusi saab kasutada erinevate kaupade, klientide või hinnagruppide puhul ning neid saab piirata kuupäevaga. Valearvestuste vältimiseks peab hinnasimulatsioonide tegemisel kaubandusleppeid arvestama. Siin on nelja tüüpi allahindlused kaubanduslepetes.

-   **Müügihind** – kaupadele saab määrata eraldi müügihinnad. Pakkumise ridade loomisel otsib programm õiget kauba müügihinda ja kannab selle pakkumise ridadele. Seetõttu ei mõjuta sellise allahindlusega kaubanduslepe hinnasimulatsiooni. Pakkumise real kasutatav müügihind kajastab kaubanduslepet.
-   **Rea allahindlus** – kaupadele määratakse spetsiaalsed allahindlused, olenevalt tellitud kogusest. Rea summasid vähendatakse harilikult rea allahindluse võrra enne hinnasimulatsiooni tegemist. Seetõttu mõjutab sellise allahindlusega kaubanduslepe hinnasimulatsiooni.
-   **Multiallahindlus** – kui kombineeritud kogused ületavad limiiti, mille olete määranud, siis käivitavad eelnevalt määratud tellitud kaupade kombinatsioonid kogu tellimuse allahindluse. Rea summasid vähendatakse harilikult rea allahindluse võrra enne hinnasimulatsiooni tegemist. Seetõttu mõjutab sellise allahindlusega kaubanduslepe hinnasimulatsiooni.
-   **Lõppallahindlus** – kui kombineeritud summad ületavad limiiti, mille olete määranud, siis käivitavad eelnevalt määratud tellitud kaupade kombinatsioonid kogu tellimuse allahindluse. Lõppallahindluse loovad pakkumise read. Kuid kuna lõppallahindlus rakendatakse pakkumise koondsummale allahindlusena, vähendab see pakkumise koondsummat. Seetõttu mõjutab sellise allahindlusega kaubanduslepe hinnasimulatsiooni.

### <a name="quotation-lines-and-trade-agreements"></a>Pakkumise read ja kaubanduslepped

Pakkumise rea loomisel või korrigeerimisel arvutatakse rea allahindlused automaatselt. Sobiv müügihind leitakse kaubale kaubandusleppe alusel.

## <a name="price-simulation-examples"></a>Hinnasimulatsioonide näited
Järgmised näited kasutavad hinna modelleerimist pakkumiste päistele ja ühe rea kaupadele.

### <a name="price-simulation-for-quotation-headers"></a>Pakkumise päiste hinnasimulatsioon

Loote pakkumise, millel on järgmised read.

-   10 ühikut kaupa BR-12 (omahind ühiku kohta 9.52 USA dollarit, müügihind ühiku kohta 15.32 USA dollarit).
-   12 ühikut kaupa BR-14 (omahind ühiku kohta 7.48 USA dollarit, müügihind ühiku kohta 13.75 USA dollarit).

Järgmine tabel näitab pakkumise ridu.

|    &nbsp;                  | Arvutus                          | Tulemus   |
|----------------------------|--------------------------------------|----------|
| Müügikogus             | 10 ühikut + 12 ühikut                  | 22 ühikut |
| Müügiväärtus USA dollarites         | (10 × 15.32) + (12 × 13.75)          | 318.20   |
| Omahind USA dollarites          | (10 × 9.52) + (12 × 7.48)            | 184.96   |
| Brutokasum USA dollarites | 318.20 – 184.96                      | 133.24   |
| Tulumäär         | (\[318.20 – 184.96\] ÷ 318.20) × 100 | 41.87%   |

Käivitate hinnasimulatsiooni ja rakendate 15-protsendise lõppallahindluse kogu pakkumisele või pakkumise päisele. Järgmine tabel näitab pakkumise uusi kogusummasid pärast hinnasimulatsiooni käivitamist.

|     &nbsp;                                           | Arvutus                               | Tulemus   |
|------------------------------------------------------|-------------------------------------------|----------|
| Müügikogus                                       | 10 ühikut + 12 ühikut                       | 22 ühikut |
| Vana müügiväärtus USA dollarites                               | (10 × 15.32) + (12 × 13.75)               | 318.20   |
| Vana omahind USA dollarites                                | (10 × 9.52) + (12 × 7.48)                 | 184.96   |
| Vana brutokasum USA dollarites                       | 318.20 – 184.96                           | 133.24   |
| Vana kasumiprotsent                               | (\[318.20 – (10 × 9.52)\] ÷ 318.20) × 100 | 41.87%   |
| 15-protsendise lõppallahindluse hinnasimulatsioon USA dollarites | (15 × 318.2) ÷ 100                        | 47.73    |
| Uus müügiväärtus USA dollarites                               | 318.20 – 47.73                            | 270.47   |
| Uus brutokasum USA dollarites                       | 270.47 – 184.96                           | 85.51    |
| Uus tulumäär                               | \[(270.47 – 184.96) ÷ 270.47\] × 100      | 31.61%   |

### <a name="price-simulation-for-single-line-items"></a>Hinnasimulatsioon ühe rea kaupade puhul

Loote pakkumise, millel on järgmised read.

-   10 ühikut kaupa BR-12 (omahind ühiku kohta 9.52 USA dollarit, müügihind ühiku kohta 15.32 USA dollarit).
-   12 ühikut kaupa BR-14 (omahind ühiku kohta 7.48 USA dollarit, müügihind ühiku kohta 13.75 USA dollarit).

Järgmine tabel näitab pakkumise ridu.

|      &nbsp;                          | Arvutus                          | Tulemus   |
|--------------------------------------|--------------------------------------|----------|
| Müügikogus                       | 10 ühikut + 12 ühikut                  | 22 ühikut |
| BR-12 müügiväärtus USA dollarites         | 10 × 15.32                           | 153.20   |
| BR-14 müügiväärtus USA dollarites         | 12 × 13.75                           | 165.00   |
| BR-12 omahind USA dollarites          | 10 × 9.52                            | 95.20    |
| BR-14 omahind USA dollarites          | 12 × 7.48                            | 89.76    |
| BR-12 brutokasum USA dollarites | 153.20 – 95.20                       | 58.00    |
| BR-14 brutokasum USA dollarites | 165.00 – 89.76                       | 75.24    |
| BR-12 kasumiprotsent USA dollarites  | \[(153.20 – 95.20) ÷ 153.20\] × 100  | 37.86    |
| BR-14 kasumiprotsent USA dollarites  | \[(165.00 – 89.76) ÷ 165.00\] × 100  | 45.60    |
| Lõppmüügiväärtus USA dollarites             | (10 × 15.32) + (12 × 13.75)          | 318.20   |
| Kogu omahind USA dollarites              | (10 × 9.52) + (12 × 7.48)            | 184.96   |
| Lõppbrutokasum USA dollarites     | 318.20 – 184.96                      | 133.24   |
| Lõppkasumiprotsent             | \[(318.20 – 184.96) ÷ 318.20\] × 100 | 41.87%   |

Käivitate hinnasimulatsiooni ja rakendate 10-protsendise lõppallahindluse BR-12 ühikutele. Järgmine tabel näitab pakkumise uusi kogusummasid pärast hinnasimulatsiooni käivitamist ühe rea kaubale.

|    &nbsp;                                         | Arvutus                             | Tulemus   |
|---------------------------------------------------|-----------------------------------------|----------|
| Müügikogus                                    | 10 ühikut + 12 ühikut                     | 22 ühikut |
| BR-12 vana müügiväärtus USA dollarites                  | 10 × 15.32                              | 153.20   |
| 10-protsendise allahindluse hinnasimulatsioon BR-12-le | (10 × 153.2) ÷ 100                      | 15.32    |
| BR-12 uus müügiväärtus USA dollarites                  | (10 × 15.32) – 15.32                    | 137.88   |
| BR-14 müügiväärtus USA dollarites                      | 12 × 13.75                              | 165.00   |
| BR-12 omahind USA dollarites                       | 10 × 9.52                               | 95.20    |
| BR-14 omahind USA dollarites                       | 12 × 7.48                               | 89.76    |
| BR-12 uus brutokasum USA dollarites          | 137.88 – 95.20                          | 42.68    |
| BR-14 brutokasum USA dollarites              | 165.00 – 89.76                          | 75.24    |
| BR-12 uus kasumiprotsent USA dollarites           | \[(137.88 – 95.20) ÷ 137.88\] × 100     | 30.95    |
| BR-14 kasumiprotsent USA dollarites               | \[(165.00 – 89.76) ÷ 165.00\] × 100     | 45.60    |
| Uus lõppmüügiväärtus USA dollarites                      | \[(10 × 15.32) – 15.32\] + (12 × 13.75) | 302.88   |
| Kogu omahind USA dollarites                           | (10 × 9.52) + (12 × 7.48)               | 184.96   |
| Uus kogu brutokasum USA dollarites              | 302.88 – 184.96                         | 117.92   |
| Uus summaarne osamaksu määr                      | \[(302.88 – 184.96) ÷ 302.88\] × 100    | 38,93%   |

Hinnasimulatsioon mõjutab ainult rida, millele see on rakendatud, ja vähendab selle rea koondsummat.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]