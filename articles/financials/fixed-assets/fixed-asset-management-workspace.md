---
title: "Põhivara halduse tööruum"
description: "Teema annab teavet põhivara halduse tööruumi kohta. See tööruum kuvab süsteemi sisestatud põhivaraga seotud andmed. See sisaldab koondvaadet ja analüüsivaadet."
author: saraschi
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c544ae60433dd14d061bc1a78d5cad6577cf579d
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-management-workspace"></a>Põhivara halduse tööruum

[!include[banner](../includes/banner.md)]

**Põhivara halduse** tööruum kuvab süsteemi sisestatud põhivaraga seotud andmed. See tööruum sisaldab koondvaadet ja analüüsivaadet. Vahekaardil **Minu töö** on kokkuvõttepaanid, põhivara üksikasjad ja seonduv teave põhivara kohta praeguses ettevõttes. Saate lisada ka otse tööruumis Power BI analüüsi jaotisse analüüse. Vahekaardil **Analüüs – kõik ettevõttes** kasutatakse Microsoft Power BI võimalusi kõigi ettevõtete põhivaraga seotud visuaalide näitamiseks.

## <a name="my-work"></a>Minu töö

### <a name="summary"></a>Kokkuvõte

Paanid jaotises **Kokkuvõte** annavad ülevaate teie põhivaradest. Nende andmete hulka kuuluvad mõõdikud veel hankimata varade kohta, jooksva aasta jooksul hangitud ja jooksval aastal likvideeritud varade kohta. Jaotises **Kokkuvõte** on olemas ka võimalus liikuda kiiresti loendilehele **Põhivara**, partii kulumisoovitusse ja põhivara töölehele.

### <a name="find-fixed-assets"></a>Põhivarade otsimine

Jaotis **Põhivarade otsimine** võimaldab otsida kiiresti varasid, sisestades põhivara numbri, grupi, nime, asukoha või vastutava isiku. Loendis kuvatakse kõik otsingukriteeriumile vastavad varad.

Loendis saate vaadata järgmisi lehti.

 - Põhivara **üksikasjade** leht
 - **Raamatute** leht kõigi põhivaraga seostatud raamatute kohta
 - **Põhivara hindamiste** leht

### <a name="valuations"></a>Hindamised

Lehel **Põhivara hindamised** saate vaadata ühelt lehelt põhivara kõige olulisemaid andmeid ja ka üksikasju kõigi põhivaraga seostatud raamatute kohta. Valik **Saldod** lehe ülemises vasakpoolses osas näitab iga põhivaraga seotud raamatu jooksvat hinnangut. Saate väärtustesse süvitsi minna, et näha üksikasjalikke kandeid, millest koondväärtus koosneb. Valik **Profiil** lehe ülemises vasakpoolses osas näitab iga põhivaraga seotud raamatu kulumigraafikut.

Lehele **Põhivara hindamised** pääseb tööruumist **Põhivara haldamine** või loendilehelt **Põhivara**.

### <a name="related-information"></a>Seostuv teave

Võite navigeerida otse lehele **Raamatute seadistus**, **Põhivarakannete päring** ja mitmesse aruandesse, kasutades linke tööruumi jaotises **Seostuv teave**.

### <a name="analytics--all-companies"></a>Analüüs – kõik ettevõtted

Lehel **Analüüs** on olulised mõõdikud põhivara kohta kõigis süsteemi juriidilistes isikutes. Juurdepääsu sellele vahekaardile juhitakse turbeprivileegiga Kõigi ettevõtte põhivarade analüüsi kuvamine.

Järgmine tabel näitab igal aruandelehel olevaid visualiseeringuid.

| Aruandeleht            | Visualiseering        |
|------------------------|----------------------|
| Põhivara hindamised | Arvestuslik jääkväärtus kokku |
| Põhivara hindamised | Raamatupidamislik jääkväärtus põhivaragrupi järgi |
| Põhivara hindamised | Soetusväärtused |
| Põhivara hindamised | Likvideerimisväärtused |
| Põhivara hindamised | Põhivara üksikasjad |
| Hindamiskaardid        | Arvestuslik jääkväärtus kokku |
| Hindamiskaardid        | Põhivara asukohad |
| Hindamiskaardid        | Põhivara üksikasjad |

Analüüsi kuvamiseks koos andmetega peate esmalt värskendama atribuudi AssetTransactionMeasure koondmõõtmist lehel **Üksuse kauplus**.

