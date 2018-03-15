---
title: Hooldustoimingud
description: "Kasutage hooldustoiminguid hooldustellimuse käigus täidetava ülesande kirjeldamiseks. Seda teavet näevad nii tehnikud kui ka kliendid."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: de180a1258bbfb95acbfd0985cb91c88efc320f2
ms.contentlocale: et-ee
ms.lasthandoff: 02/21/2018

---

# <a name="service-tasks"></a>Hooldustoimingud  

[!include[banner](../includes/banner.md)]

Kasutage hooldustoiminguid hooldustellimuse käigus täidetava ülesande kirjeldamiseks.
Seda teavet näevad nii tehnikud kui ka kliendid.

Hooldustoimingute loomine toimub lehel **Hooldustoimingud** ning te seostate hooldustoimingud kindla hooldusleppe või hooldustellimusega, luues hooldustoimingu seose. Iga kord, kui loote hooldustoimingu seose, saate luua järgmise.

-  Sisemärkused ülesande kohta, nagu detailsed tehnilised nõudmised ülesandele, mida tehnikul on vaja teada.

-  Välised märkused, mida klient näeb. Need võivad anda töös oleva ülesande kohta vähem tehnilise selgituse vastavalt kokkuleppele kliendi ja hooldusettevõtte vahel.

Kui olete loonud hooldustoimingu seose hooldustoimingu ja hooldustellimuse vahel, saate täpsustada seda hooldustoimingut, kui loote hooldustellimusele või hooldusleppele ridu.

Kui loote hooldustellimusi hooldusleppe põhjal, siis saate kasutada hooldustoiminguid, mis on määratud igale hooldusleppe reale hooldustellimuse ridade grupeerimiseks hooldustellimustesse.

## <a name="create-a-service-task"></a>Hooldustoimingute loomine

1. Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Hooldustoimingud**.
2. Looge uus rida.
3. Sisestage teenuse ID ja kirjeldus.

## <a name="example"></a>Näide

Tehnikul on vaja täita kaks tööülesannet käigukasti juures (teenusobjekt GB-1234) kliendi asukohas. Kliendile luuakse hoolduslepe ja tööülesannetega seostatakse mitu kannet. Hoolduslepe ja leppe read kahe tööülesande kohta on järgmised.

### <a name="service-agreement"></a>Hoolduslepe

| Projekt | Hoolduslepe | Kirjeldus                                  | Grupeeri   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Kontroll ja rutiinne asendamine – GB-1234 | Preemia |

### <a name="service-agreement-lines"></a>Hooldusleppe read

| Kirjeldus             | Kande tüüp | Teenuse objekt | Hooldustoiming |
|-------------------------|------------------|----------------|--------------|
| Kontrollimine ja puhastamine | Tund             | GB-1234        | I/C - GB1234 |
| Reisimine                  | Expense          | GB-1234        | I/C - GB1234 |
| Materjalid               | Kaup             | GB-1234        | I/C - GB1234 |
| Rutiinne asendamine     | Tund             | GB-1234        | RR - GB1234  |
| GR-1                    | Kaup             | GB-1234        | RR - GB1234  |
| GR-5                    | Kaup             | GB-1234        | RR - GB1234  |

Kahe tööülesande hooldusleppe ridadele on lisatud kaks hooldustoimingut. Hooldustoimingud määravad kanded, mis iga tööülesande alla kuuluvad. Esimesel juhul näitab hooldustoiming I/C - GB1234 kõiki hooldusleppe ridu, mis on seotud objekti GB-1234 kontrollimise ja puhastamisega. Teisel juhul näitab hooldustoiming RR - GB1234 kõiki hooldusleppe ridu, mis on seotud rutiinse asendamisega.

Hooldustoimingu seosed, mis ühendavad hooldustoiminguid kindla leppega, on järgmised.

### <a name="service-tasks"></a>Hooldustoimingud

| Hooldustoiming | Kirjeldus                             | Sisemärkus                                                                                                                 | Väline märkus                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Käigukasti GB-1234 kontrollimine           | Käigukasti GB-1234 visuaalne ja mehaaniline kontrollimine ja puhastamine                                                              | Käigukasti rutiinne kontrollimine |
| RR - GB1234  | GB-1234 osade rutiinne asendamine | Rutiinse teenuse käigus GR-1 ja GR-5 komponentide asendamine (enne 2002. aastat valmistatud käigukastide puhul asendatakse ka GR-2 komponent) | Rutiinne osade asendamine  |

## <a name="group-service-orders"></a>Hooldustellimuste grupeerimine

Kui loote automaatselt hooldustellimusi, siis saate kasutada hooldustoimingut grupeerimise kriteeriumina. Hooldustoimingute grupeerimiseks määrake hooldusleppes, et hooldusleppel põhinevad hooldustellimused tuleb grupeerida hooldustoimingu ID järgi, mis on nende esmane grupeerimiskriteerium.

**Grupeerimine hooldustoimingute kaupa**

1. Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.
2. Vahekaardil **Häälestus** valige väljal **Hooldustellimuste ühendamine** valik **Hooldustoimingu alusel**.


