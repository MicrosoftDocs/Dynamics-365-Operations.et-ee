---
title: Kontsernisisene planeerimine
description: See artikkel kirjeldab kontsernisisest plaanimist ja selgitab, kuidas konfigureerida kontsernisisest plaanimist koos Microsofti plaanimise optimeerimisega Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 65467fd9525ae8fb5a65a9316b7307f611fa6e42
ms.sourcegitcommit: ec15857b753ebedd86503170efd54c8007b87231
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475608"
---
# <a name="intercompany-planning"></a>Kontsernisisene planeerimine

[!include [banner](../../includes/banner.md)]

Mõnede organisatsioonide puhul sõltuvad logistikatoimingud organisatsiooni muudest juriidilistest isikutest (ettevõtetest). Neid toiminguid käsitletakse kontsernisiseste müügitehingute ja ostude abil, kuna igal juriidilisel isikul on eraldi kontoplaan.

See artikkel kirjeldab kontsernisisest plaanimist ja selgitab, kuidas konfigureerida kontsernisisest plaanimist koos Microsofti plaanimise optimeerimisega Dynamics 365 Supply Chain Management.

Selles artiklis kasutatakse järgmisi olulisi kontsernisiseseid tingimusi:

- **Ülesvoolu** – suhteline viide firmas või tarneahelas. See näitab liikumist toormaterjali tarnija suunas.
- **Allavoolu** – suhteline viide firmas või tarneahelas. See näitab liikumist kliendi suunas.
- **Plaanitud kontsernisisene nõudlus** – plaanitud nõudlus toote järele ettevõttes, põhinedes plaanitud nõudlusel, mis on allavoolu ettevõttel toote järele.

Koondplaneerimise puhul võib ühe ettevõtte plaan sisaldada plaanitud kontsernisisest nõudlust, mis on seotud plaanitud tellimustega teises ettevõttes. See võimalus on kasulik, kuna see võimaldab ettevõtete plaanitud tellimuste täieliku nähtavuse. See tagab ka, et kõik nõutavad plaanitud tarnetellimused on loodud, kuid eeldamata plaanitud tellimuste kinnitamist kontsernisisese nõudluse jaoks.

Kui alustate koondplaneerimist põhiplaanist, mis sisaldab plaanitud allavoolu nõudlust, lisatakse plaanile nõudlusena seotud kontsernisiseste hankijate plaanitud ostutellimused.

## <a name="required-setup"></a>Nõutav häälestus

Kontsernisisese planeerimise kasutamiseks peate oma süsteemi ette valmistama järgmisel viisil.

1. Asjaomased tooted tuleb vabastada kõikides asjaomastes ettevõtetes. Lisateavet vt jaotisest Kontsernisisese [kaubanduse konfigureerimine ja kasutamine Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Allavoolu nõudlus peab olema kaetud ostudega hankijalt, kellel on kontsernisisesed seosed ülesvoolu ettevõttega ja asjakohased vaikimisi varude dimensioonid (sait ja ladu) kliendi kohta. Lisateavet vt jaotisest Kontsernisisese [kaubanduse konfigureerimine ja kasutamine Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Ülesvoolu ettevõtte koondplaan peab sisaldama plaanitud allavooluetapi nõudlust ning allavoolu plaanides tuleb määrata vastav ettevõte ja koondplaan.

## <a name="include-planned-downstream-demand"></a>Kaasa plaanitud järgmise etapi nõudlus

Järgige neid juhiseid, et konfigureerida oma koondplaan nii, et see hõlmaks plaanitud allavoolu nõudlust.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige või looge koondplaan.
1. Määrake kiirkaardil **Kontsernisisene plaanimine** järgmised väljad.

    - **Lisa plaanitud allavooluetapi nõudlus** – määrake selle suvandi väärtuseks *Jah*, et võimaldada koondplaneerimise kontsernisisest plaanimist.
    - **Allavooluetapi plaanid** – kui määrate suvandi **Lisa plaanitud allavooluetapi nõudlus** väärtuseks *Jah*, kasutage teiste ettevõtete soovitud koondplaanide lisamiseks tööriistariba ja ruudustikku.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Ettevõtete sidumine mitmetasandilise sidumise abil

Mitmetasandilise sidumise puhul saate kuvada seotuse kõigis ettevõtetes, et näha algset nõudluse allikat, mida tarne hõlmab.

Mitmetasandilise sidumise teabe vaatamiseks toimige järgmiselt.

1. Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**.
1. Valige või avage plaanitud tellimus.
1. Seejärel valige toimingupaanil vahekaardi **Vaade** grupis **Nõuded** suvand **Mitmetasandiline sidumine**.

### <a name="intercompany-example-that-involves-two-companies"></a>Kontsernisisene näide, mis hõlmab kaht ettevõtet

Selles näites luuakse plaanitud tootmistellimus ettevõttes USMF, et katta müügitellimus ettevõttes DEMF. USMF-is on otsene nõudlus plaanitud kontsernisisene nõudlus. Selle nõudluse kuvamiseks USMF-is käivitub koondplaneerimine esmalt DEMF-is ja seejärel USMF-is.

Järgmine illustratsioon näitab, kuidas see näide võidakse kuvada plaanitud tootmistellimuse lehel **Mitmetasandiline sidumine**.

![Kontsernisisene näide, mis hõlmab kaht ettevõtet.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Kontsernisisene näide, mis hõlmab kolme ettevõtet

Selles näites luuakse plaanitud ostutellimus ettevõttes USMF, et katta müügitellimus ettevõttes FRRT. Ettevõttes DEMF ja USMF on otsene nõudlus plaanitud kontsernisisene nõudlus. Selle nõudluse kuvamiseks USMF-is käivitub koondplaneerimine esmalt FRRT-is, seejärel DEMF-is ja lõpuks USMF-is.

Järgmine illustratsioon näitab, kuidas see näide võidakse kuvada plaanitud tootmistellimuse lehel **Mitmetasandiline sidumine**.

![Kontsernisisene näide, mis hõlmab kolme ettevõtet.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
