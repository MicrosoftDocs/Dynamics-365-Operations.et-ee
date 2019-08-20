---
title: Töötellimuste loomine hooldustaotluste põhjal
description: See teema selgitab, kuidas luua varahalduses hoolduse päringust töökäsk.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f7af87f359cfe3a606c8be857dd905bfef75e97
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847455"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Töötellimuste loomine hooldustaotluste põhjal

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Pärast hoolduspäringute loomist saate need hõlpsalt töötellimusteks teisendada. See teema kirjeldab kiireimat viisi, kuidas töötada hooldustaotlustega, uuendada mitut hooldustaotlust korraga ja seejärel luua töökäsk mitme hooldustaotluse jaoks samal ajal. Lehel **Aktiivsed hooldustaotlused** või lehel **Minu funktsionaalsed asukohahoolduse taotlused** saate töötada korraga ka ühe hooldustaotlusega ja teisendada ühe hooldustaotluse töötellimuseks.

> [!NOTE]
> Iga hooldustaotlus võib olla seotud ainult ühe töötellimusega. Mitu hooldustaotlust saab siiski lisada ühele töötellimusele, isegi kui hooldustaotlustes on erinevad varad.

1. Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Hooldustaotlused**.
2. Enne kui saate hooldustaotlusest töökäsu luua, peate hooldustaotluse jaoks valima vähemalt hooldustöö tüübi ja hooldustöö tüübi variandi ning kaubanduse, kui see teave on asjakohane. Ruudustiku vaates saate hõlpsasti värskendada hooldustaotluse teavet.
3. Kui olete valmis töökäsu looma, valige sellesse kaasatavad hooldustaotlused.

    - Kui valite töötellimuseks teisendamiseks mitu hooldustaotlust, tuleb enne töökäsu loomist häälestada mõlemad väljad: **Vara** ja **Hooldustöö tüüp**.
    - Kui valite töötellimuseks teisendamiseks ühe hooldustaotluse, tuleb enne töökäsu loomist häälestada üksnes väli **Vara**. Töökäsu loomisel saate siiski valida hooldustöö tüübi (ja seotud hooldustöö tüübi variandi ja kaubanduse, kui see teave on asjakohane) dialoogiboksis **Loo töötellimus**.

4. Valige **Töökäsk**.
5. Dialoogiboksis **Loo töökäsk** sätestage väljad ja seejärel klõpsake nuppu **OK**.

    Teateriba võib teid teavitada, et on loodud uus töökäsk.

    Lisaks, kui loote töökäsu, mis põhineb hoolduse taotlusel, kui hoolduse taotlusega seotud vara sisaldub garantiilepingus, teavitab teateriba teid garantiilepingust.

6. Valige **Varahaldus**\>**Ühised**\>**Töökäsud**  \>**Kõik töökäsud** ja avage uus töökäsk.

    ![Joonis 1](media/05-manage-maintenance-requests.png)

