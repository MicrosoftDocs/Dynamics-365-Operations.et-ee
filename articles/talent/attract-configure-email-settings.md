---
title: Meilisätete konfigureerimine rakenduses Microsoft Dynamics 365 Talent – Attract
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 Talent - Attract saadetud e-posti sätteid.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008658"
---
# <a name="configure-email-settings"></a>Meilisätete konfigureerimine

[!include[banner](../includes/banner.md)]

Teie kaubamärk loob usalduse ja aitab teil luua suhteid kandidaatidega, enne kui nad isegi teie vabadele töökohtadele kandideerivad. Positiivne kaubamärgi taju meelitab parimaid talente ja suurendab olemasolevate töötajate lojaalsust. Microsoft Dynamics 365 Talent: Attract võimaldab teil konfigureerida e-kirju nii, et need peegeldavad teie ettevõtte kaubamärki. Seetõttu saate pakkuda töökoha kandidaatidele järjepideva kogemuse, kui nad läbi kandideerimisprotsessi edenevad.

Attract võimaldab teil teha järgmisi toiminguid.

- Konfigureerige e-posti sätted nii, et kasutatakse teie ettevõtte Microsoft Exchange'i e-posti teenuse kontot. Sel viisil teavad kandidaadid, et meilid tulevad teie ettevõttest. Näiteks saate konfigureerida sätteid nii, et kandidaadid saavad e-kirju aadressilt `recruiting@contoso.com`, mitte `contoso@microsoft.com`.
- Loogu kogu meilisuhtlusele ühtne tootjakohanduse, määrates kõigile meilimallidele üldine päis ja jalus. 

> [!NOTE]
> Attracti häälestamiseks, nii et see kasutaks meilide saatmiseks teie ettevõtte meiliteenuse kontot, vajate tervikliku värbamise lisandmoodulit.

## <a name="connect-an-email-service-account"></a>E-posti teenuse konto ühendamine

Ühendades oma ettevõtte meiliteenuse konto, saate luua kaubamärgiga e-posti kogemuse oma kandidaatidele. Kui te oma ettevõtte kontot ei ühenda, kasutab Attract vaikimisi Microsofti kaubamängiga meiliteenuste kontot.

1. Valige lehe paremast ülanurgast hammasratta sümbol **Sätted** ja seejärel valige **Halduskeskus**.
2. Vahekaardil **Meilisätted** valige jaotises **Meiliteenuste kontod** suvand **Ühenda ettevõtte konto**.

    ![Oma ettevõtte meiliteenuse konto ühendamine Attractis](./media/attract-admin-email-service-accounts.png)

    Lisateavet ühiskasutatava meilikonto loomise kohta vt teemast [Ühiskasutatavad postkastid rakenduses Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. Logige Microsofti sisselogimise aknas sisse, kasutades oma ettevõtte mandaate.
4. Kui te ei ole veel meiliteenuse kontot seadistanud või kui soovite lisada uue, valige käsk **Lisa uus teenusekonto**ja sisestage seejärel oma e-posti andmed. Kui olete juba selle meiliteenuse konto seadistanud, mida soovite kasutada, valige see.

Kui teie meiliteenuse konto on edukalt konfigureeritud, kuvatakse see jaotises **Meiliteenuse kontod**.

## <a name="disconnect-an-email-service-account"></a>E-posti teenuse konto eemaldamine

Kui soovite lõpetada oma ettevõtte domeeni kasutamise Attracti meiiteenuses, saate meiliteenuse konto eemaldada.

1. Valige lehe paremast ülanurgast hammasratta sümbol **Sätted** ja seejärel valige **Halduskeskus**.
2. Valige vahekaardil **Meilisätted** jaotises **Meiliteenuste kontod** nupp **Veel** (kolm vertikaalset punkti) selle meiliteenuste konto kõrval, mida soovite eemaldada.
3. Valige **Eemalda meilikonto**.

    ![Oma ettevõtte meiliteenuse konto eemaldamine](./media/attract-admin-disconnect-email-account.png)

4. Kui teil palutakse toiming kinnitada, valige **Katkesta ühendus**.

    ![Oma ettevõtte meiliteenuse konto eemaldamise kinnitamine](./media/attract-admin-email-confirm-disconnect.png)

Kui te ei ühenda erinevat meiliteenuste kontot, saadetakse Attractist saadetud meilid vaikimisi kasutades Microsofti kaubamärgiga meiliteenuste kontot.

## <a name="configure-email-template-settings"></a>E-kirja malli sätete konfigureerimine

Saate laadida üles pilti oma ettevõtte logost või muid andmeid oma meilide kohandatud päise jaoks. Saate anda meili jaluses ka linke oma privaatsuspoliitikale ja kasutustingimustele.

> [!NOTE]
> Peate järgima oma riigi või piirkonna kohaldatavaid seadusi ja samuti selle riigi või piirkonna seadusi, mille alla kuulub meili saaja. Need seadused hõlmavad rämpsposti vastaseid reegleid.

1. Valige lehe paremast ülanurgast hammasratta sümbol **Sätted** ja seejärel valige **Halduskeskus**.
2. Lohistage vahekaardil **Meilisätted** jaotises **E-kirja malli sätted** oma meilide päises kasutada soovitud pilt pildiaknasse või sirvige vastava faili leidmiseks. Olemasoleva pildi asendamiseks peate esmalt valima selle kõrval suvandi **Eemalda**. Pilt peab olema JPEG, JPG, PNG või SVG fail. Piltide soovituslik suurus on vahemikus 25 – 800 pikslit (laius) ja 25 – 150 pikslit (kõrgus). Päise maksimaalne failimaht on 1 megabaiti (MB).

    ![Teie ettevõtte e-posti päise jaoks pildi lisamine](./media/attract-admin-email-header.png)

3. Andke jaotises **Teie suhtlusele kohaldatav privaatsuspoliitika** link teie ettevõtte privaatsuspoliitikale. Andke jaotises **Teie suhtlusele kohaldatavad tingimused** link teie ettevõtte kasutustingimustele.

    ![Oma ettevõtte privaatsuspoliitika ja kasutustingimuste linkide lisamine e-posti jalusele](./media/attract-admin-email-footer.png)

4. Valige **Salvesta**, et salvestada e-kirja malli sätted.
