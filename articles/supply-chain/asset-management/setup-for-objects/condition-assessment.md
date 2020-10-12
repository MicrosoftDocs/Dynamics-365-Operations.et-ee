---
title: Seisundi hindamine
description: Selles teemas selgitatakse, kuidas koostada seisundi hindamise malli ja registreerida vara varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 774c788959c5ebea69b4d22c886ac673f50b97f5
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889789"
---
# <a name="condition-assessment"></a>Seisundi hindamine

[!include [banner](../../includes/banner.md)]

 

Selles teemas selgitatakse, kuidas koostada seisundi hindamise malli ja registreerida vara varahalduses. Seisundi hindamine toimub korrapäraste ajavahemike järel ning esmane eesmärk on luua ja säilitada vara tingimusandmed. Ennetava hoolduse seisukohast on oluline jälgida põhiteavet, näiteks praegust seisundit ja järelejäänud eluiga. Lisaks, kui teete seisundi hindamist korrapäraste ajavahemike järel, siis on teil võimalik jälgida ja võrrelda tingimusi masinatel oma tehases.

Seisundi hindamist saab kasutada, et mõõta ja jälgida paljusid tingimusi teie seadmetel. Näide: te võite mõõta oma masinate vibratsioone. Pärast seda, kui olete registreerinud vibratsiooni mõõtmised varahalduses eri tüüpi seadmete kohta, saate otsida viimaseid registreeritud hinnangut ja vaadata vibratsiooni mõõtmisi.

Seisundi hindamine on loodud varadele. Enne tingimuse hindamise protseduuri tegemist seadistage vara tüübi seisundi hindamise mall. Põhjus mallide kasutamiseks seisundi hindamisel on vältida sarnaste varade tingimusandmete varieerumist. Seisundi hindamise seadistamise ja kasutamise järjestus varahalduses on järgmine: esmalt seadistage nõutavad seisundi hindamise mallid. Järgmisena seostage mallid varade tüüpidega vormil **Varade tüübid**. Lõpuks saate luua seisundi hindamise registreerimisi vara kohta vormil **Vara**.

## <a name="create-a-condition-assessment-template"></a>Seisundi hindamismalli loomine

1. Valige **Varahaldus** > **Häälestus** > **Varade tüübid** > **Seisundi hindamine**.
2. Valige uue malli loomiseks **Uus**.
3. Sisestage malli ID väljale **Mall**.
4. Sisestage malli nimi väljale **Nimi**.
5. Lisage kiirkaardile **Seisundi hindamise read** nõutavad read seisundi hindamiseks, sealhulgas sobiva tingimuse tüüp ja mõõtühik.
6. Kiirkaardile **Vara tüübid** lisage vara tüübid, mille puhul peaks kasutama tingimuse hindamise malli.
7. Väljadel **Read** ja **Vara tüübid** lehe ülaosas rühmas **Üksikasjad** kuvatakse valitud tingimuse hindamismalliga seotud hinnanguridade ja varatüüpide arv.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Vara seisundi hindamise registreerimise loomine

1. Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad**.
2. Valige loendist või hankija, kellele soovite kontakti luua.
3. Klõpsake vahekaardi **Üldine** nuppu **Hõlbustusvahendid**.
4. Uue reegli loomiseks klõpsake valikut **Uus**.
5. Valige seisundi hindamise kuupäev väljal **Kuupäev**.
6. Valige töötaja nimi, kes tegi hinnangu registreerimise väljal **Töötaja**.
7. Väljal **Read** näete seisundi hindamisel seadistatud hindamisridade arvu.
8. Valige mall seisundi hindamiseks väljal **Mall**. Malli nimi sisestatakse automaatselt väljale **Nimi** ja seotud registreerimisread sisestatakse kiirkaardile **Seisundi hindamise read**.
9. Kiirkaardile **Märkmed** saate sisestada valitud seisundi hindamisega seotud märkmeid.
10. Iga seisundi hindamise rea kohta sisestage mõõtmisandmed väljale **Väärtus**.
11. Saate sisestada valitud registreerimisreaga seotud kommentaari kiirkaardi **Seisundi hindamise read** väljale **Kommentaarid**. Kui lisate reale kommentaari, valitakse automaatselt märkeruut **Kommentaar**.

Pärast seda, kui olete teinud seisundi hindamise registreerimise, saate seisundi hindamise aruande printida.

>[!NOTE]
>Samuti saate registreerida seisundi hindamise töökäsul (**Varahaldus** > **Ühised** > **Töökäsud** > **Kõik töökäsud** > **Seisundi hindamise** nupp.)
