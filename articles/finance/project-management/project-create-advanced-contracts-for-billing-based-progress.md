---
title: Valmidusastmelisusel põhineva arveldamise täpsemate lepingute koostamine
description: See teema selgitab, kuidas luua projektilepinguid, et saaksite luua klientidele arveid, mis põhinevad lõpuleviidud töö protsendil.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282821"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Valmidusastmelisusel põhineva arveldamise täpsemate lepingute koostamine
[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas luua projektilepinguid, et saaksite luua klientidele arveid, mis põhinevad lõpuleviidud töö protsendil. Projekti jaoks seadistatavate töö eelarvekategooriate jaoks arvutatakse arvete summad automaatselt. Arvete ajastus seadistatakse siis, kui lepite kliendiga projektilepingu tingimustes kokku.

Kasutage selles teemas toodud protsesse, et seadistada leping, seostatud projekt ja arveldusreeglid, mida kasutatakse arvesummade arvutamiseks projekti jaoks seadistatud töö eelarvekategooriate puhul.

Pärast lepingu ja projekti loomist saate seadistada projekti üksikasjad. Näiteks saate määratleda projekti tegevused ja määrata projekti töötajaid.

## <a name="example"></a>Näide

Teie organisatsioon on tarkvaraarenduse firma. Lepite kokku, et arendate kliendile palgaarvestuse paketi kokku 20 000 USA dollari (USD) eest. Teie organisatsioon nõustub saatma kliendile arve, kui projekti konkreetsed protsentuaalsed osad saavad valmis. Te seadistate töö jaoks järgmised projektikategooriad, et saaksite neid kasutada arveldusprotsessis.

- Nõustamine
- Kujundus
- Install

Samuti seadistate arveldusreeglid, mis arvutavad automaatselt arvesummad igas kategoorias lõpuleviidud projekti töö protsendi jaoks.

Eelarvejuht loob projektikategooriate eelarve. Lõpuleviidud töö hulk arvutatakse automaatselt protsentidena, võrreldes eelarvelist hulka tegeliku tööga.

## <a name="prerequisites"></a>Eeltingimused

Enne kui loote projekti, mis kasutab arveldusreegleid, peate seadistama arveldusreeglite jaoks numbriseeriad ja tasu töölehe, mida kasutatakse valmidusastmelise arvelduse sisestamiseks.

1. Avage **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.
2. Seadistage lehel **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Numbriseeriad** need numbriseeriad, mida soovite arveldusreeglite loomisel kasutada.
3. Avage **Projektihaldus ja raamatupidamine** \> **Töölehed** \> **Tasu**.
4. Valige lehel **Tasu tööleht** valik **Uus** ja sisestage töölehe nimi.

## <a name="create-a-contract-for-progress-billings"></a>Valmidusastmelise arvelduse lepingu loomine

Selle toimingu abil saate luua projektilepingu fikseeritud hinnaga projekti jaoks. Saate luua projekti arve, kui projektis lõpuleviidud töö hulk jõuab kindlaksmääratud protsendimäärani.

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Projektilepingud**.
2. Lehel **Projektilepingud** valige suvand **Uus**.
3. Dialoogiboksis **Uus projektileping** määrake järgmised väljad.

    - **Nimi**
    - **Rahastamise tüüp**
    - **Rahastamise allikas**
    - **Müügivaluuta** – vaikimisi kasutatakse seda valuutat kliendiarvete jaoks, mis on seostatud projektilepinguga. Siiski saate muuta kindla kliendiarve müügivaluutat.

4. Valige nupp **OK**. Teave kopeeritakse lehe **Projektilepingud** päisele.
5. Täitke lehel **Projektilepingud** ülejäänud nõutud teave projekti jaoks.

## <a name="create-a-project-for-progress-billings"></a>Valmidusastmelise arvelduse projekti loomine

Järgige neid samme, et luua projekt ja mis tahes alamprojektid, mis on projektilepinguga seostatud.

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.
2. Valige lehel **Kõik projektid** suvand **Uus**.
3. Valige dialoogiboksis **Uus projekt** väljal **Projekti tüüp** suvand **Aeg ja materjal**.
4. Valige projektigrupp. Projektigrupp määratleb sisestusteabe projektidele, mis on gruppi määratud.
5. Valige **Loo projekt**.
6. Pärast projekti loomist seatakse projekti etapi olekuks **Pooleli**.

## <a name="create-a-budget-for-a-project"></a>Projekti eelarve loomine

Eelarvekategooriaid kasutatakse automaatselt kliendile arvesummade arvutamiseks igas kategoorias lõpetatud töö protsendi kohta. Järgige neid samme hinnanguliste maksumuste eelarvekategooriate loomiseks.

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.
2. Valige lehel **Kõik projektid** soovitud projekt ja avage see.
3. Valige lehe **Projektid** toimingupaanil vahekaardi **Plaan** grupis **Eelarve** valik **Projekti eelarve**.
4. Sisestage lehel **Projekti eelarve** projekti iga kategooria hinnanguline maksumus.

## <a name="create-billing-rules-for-progress-billings"></a>Valmidusastmelise arvelduse arveldusreeglite loomine

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Projektilepingud**.
2. Valige lehel **Projektilepingud** projektileping ja avage see.
3. Valige projektilepingu lehel kiirkaardil **Arveldusreeglid** valik **Lisa**.
4. Valige lehel **Arveldusreeglid** väljal **Rea tüüp** valik **Edenemine**.
5. Sisestage kiirkaardil **Arveldusreegli rea üksikasjad** väljale **Lepingu väärtus** lepingu koguväärtus.
6. Väljal **Kategooria** valige soovitud kategooria tasu kande sisestamiseks.
7. Väljal **Projekt** valige projekt või ülesanne, mis kasutab seda arveldusreeglit.
8. Valikuline: määrake arvereegel teistele projektidele. Valige projekt kiirkaardi **Projekt** jaotises **Saadaolevad projektid** ja seejärel valige parem noolenupp, et lisada projekt jaotisse **Valitud projektid**.
9. Valikuline: arvutage protsendimäär, mida klient arve maksetest kinni peab. Kiirkaardil **Makse kinnipidamise tingimused** valige rahastamisallikas ja sisestage seejärel väljale **Kinnipidamise protsent** kinnipidamise protsent.
10. Korrake neid samme, et luua projektilepingu jaoks täiendavad arveldusreeglid.
