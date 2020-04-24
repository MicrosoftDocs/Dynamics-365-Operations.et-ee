---
title: Töötellimuste loomine hooldustaotluste põhjal
description: See teema selgitab, kuidas luua varahalduses hoolduse päringust töökäsk.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205203"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Töötellimuste loomine hooldustaotluste põhjal

[!include [banner](../../includes/banner.md)]

 


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

    ![Uue töökäsu avamine](media/05-manage-maintenance-requests.png)

