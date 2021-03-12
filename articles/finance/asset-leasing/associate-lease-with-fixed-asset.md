---
title: Põhivara seostamine rendiga
description: See teema selgitab, kuidas seostada olemasolev põhivara uue rendikirjega.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 274fcc73b48282a8025a210dd488105500609d5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971424"
---
# <a name="associate-fixed-assets-with-leases"></a>Põhivara seostamine rendiga

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas seostada olemasolev põhivara uue rendikirjega. Kui seostate põhivara rendikirjega, on põhivara soetusmaksumuseks kasutamisõiguse esemeks oleva vara väärtus esialgsel tuvastamisel.

Enne põhivara rendiga seostamist peate looma põhivara jaoks suvandis Põhivarad kirje. Seejärel peate looma lehel **Rendi kokkuvõte** rendikirje ja seostama vara selle rendiga.

1. Lisage rendikirje, järgides samme teemas [Rendikirjete lisamine või kopeerimine](add-lease.md). Valige lehel **Rendikirje lisamine** väljale **Põhivara number** vara, mis ei ole veel soetatud.
2. Valige suvand **Raamatud** ja kinnitage maksegraafik.
3. Valige suvand **Esialgne tuvastamine**.
4. Valige suvand **Vara rentimise tööleht**.

    Rendikirje algse tuvastamise töölehe kirje debiteerib põhivara summas, mis on tavaliselt debiteeritud kasutamisõiguse esemeks oleva vara kontoga.

    Saate nüüd kuvada põhiraamatu tehingu tüübi ja raamatu.

5. Valige **Töölehe üksikasjad**.
6. Valige **Read**, et vaadata töölehe kirje üksikuid ridu.
7. Valige vara sisaldav töölehe rida ja valige seejärel vahekaart **Põhivarad**.

    Vahekaart **Põhivarad** kuvab kande tüübi ja raamatu. Vaikimisi on väli **Tehingu tüüp** määratud valikule **Omandamine** ja väli **Raamat** on määratud põhivara praegusele raamatule.

Pärast esialgse tuvastuse töölehe kirje sisestamist kuvatakse kanne põhivara soetamise kandena. Kannete tabeli vaatamiseks avage jaotis **Põhivarad \> Põhivarad \> Põhivarad**, valige vastav vara ja valige seejärel **Hindamised**. Peaksite nägema, et esialgse tuvastuse töölehe kirje sisestamine on loonud määratud põhivara jaoks soetamise kande.

Põhivara saab nüüd amortiseerida põhivarade standardse kulumi funktsiooni abil. Lisateavet kulumiarvestuse kohta leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Kui seostate põhivara rendiga, on nupud **Vara kulum** ja **Rendi väärtuse langus** põhivara rentimises keelatud. Vara kulumist ja rendi väärtuse languse tehinguid saate vaadata püsivaradest. Nupp **Vara kanded**, mis avab päringu vormi, on samuti keelatud. Saate avada päringu **Vara tehingud** ka põhivaradest.  
