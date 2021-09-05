---
title: Põhivara seostamine rendiga
description: See teema selgitab, kuidas seostada olemasolev põhivara uue rendikirjega.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd55d433b0961b8b210b9c28d7340ff880635a85
ms.sourcegitcommit: 3af457fc216bd0020843291ca57fd379acb53c96
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/17/2021
ms.locfileid: "7392470"
---
# <a name="associate-fixed-assets-with-leases"></a>Põhivara seostamine rendiga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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

Kui rent on seotud põhivaraga, uuendatakse põhivararaamatu **Teenusea** väli nii, et see ühtiks väikseima väärtusega järgmistest kriteeriumidest: 

 - Vara kasulik tööiga
 - Rendi tähtaeg seotud rendiraamatust

Kui välja **Omandiõiguse üleminek** väärtuseks on rendiraamatu puhul määratud **Jah**, on välja **Kasutusiga** väärtus alati vara kasulik tööiga. 
 
Kasutusiga uuendatakse iga kord, kui renti korrigeeritakse, et tagada vara kasutusaja amortiseerimine tähtajalise rendi korral, nagu oleks see amortiseeritud Varade kulumis.

> [!NOTE]
> Kui seostate põhivara rendiga, on nupud **Vara kulum** ja **Rendi väärtuse langus** põhivara rentimises keelatud. Vara kulumist ja rendi väärtuse languse tehinguid saate vaadata püsivaradest. Nupp **Vara kanded**, mis avab päringu vormi, on samuti keelatud. Saate avada päringu **Vara tehingud** ka põhivaradest.  

Lehekülgedel **Põhivarad** ja **põhivararaamat** kuvatakse põhivaraga seostatud liisingu ID. Kui põhivara on seotud rendiga, kuvatakse liisimise ID ja liisingu kirjeldus põhivarade lehel **renditeabe** kiirkaardil **Põhivara** lehel. Liisinguraamatutega seotud põhivararaamatute puhul kuvatakse väljadel **Liisingu ID**, **Liisingu kirjeldus** ja **Raamatu tüüp** valitud põhivararaamatu teave **Liisinguteabe** kiirkaardil, näitamaks, et see on seotud rendiraamatuga.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
