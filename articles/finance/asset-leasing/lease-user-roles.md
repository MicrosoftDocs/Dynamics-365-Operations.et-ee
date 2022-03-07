---
title: Rendi kasutajarollide määramine
description: See teema kirjeldab varade rentimisel kasutatavaid turberolle. Lisaks selgitatakse, kuidas määrata nendele rollidele kasutajaid.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7a3443cf9fa5b14ac0b3c4560ed45874939aa50cd665f4db46290f5af04bf6ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771748"
---
# <a name="assign-lease-user-roles"></a>Rendi kasutajarollide määramine

[!include [banner](../includes/banner.md)]

See teema kirjeldab varade rentimisel kasutatavaid turberolle. Lisaks selgitatakse, kuidas määrata nendele rollidele kasutajaid.

Vara rentimisele juurdepääsu eristavad kolm kasutajarolli. Üks on sobiv rentide haldamiseks, üks sobiv rentide vaatamiseks ja üks sobiv rentniku kohustuste täitmiseks. Igal rollil on iga rendi lehe jaoks kindlad õigused ja võimaldab igal kasutajal vaadata, luua, muuta või kustutada rente vastavalt oma töökohustustele.

| Roll           | Kirjeldus |
|----------------|-------------|
| Rendi haldamine | Selle rolliga kasutajad saavad rente lisada, muuta, kustutada ja vaadata. See roll on mõeldud igapäevastele kasutajatele, kelle ülesannete hulka kuuluvad igakuise töölehe kirjete loomine ja sisestamine ning uute rendikirje lisamine. See roll annab juurdepääsu kõikidele vara rentimise funktsioonidele. |
| Rendi kuvamine     | Selle rolliga kasutajad saavad ainult vaadata rendi kirjeid, ajakavu ja käitada aruandeid. Nad ei saa luua uusi rendikirjeid, muuta olemasolevaid rente ega luua töölehe kandeid rendi suhtes. Roll on mõeldud kasutajatele, kes peavad vaid vaatama rente, rendi ajakavasid ja tehinguid, mis selle rendikirjega seoses aset leiavad. |
| Rendtnik    | Selle rolliga kasutajad saavad luua ainult uusi rendikirjeid. Nad ei saa muuta ega kustutada olemasolevaid rendikirjeid, vaadata rendi ajakavasid ega sisestada rentimise töölehe kandeid. See roll on mõeldud kasutajatele, kes töötavad andmesisestuse võimalusega. |

Järgige järgmisi etappe, et määrata kasutajatele rollid, mida vara rentimisel kasutatakse.

1. Minge jaotisesse **Süsteemihaldus \> Turve \> Kasutajate rollidesse määramine**.
2. Valige roll **Rendi haldamine**, **Rentnik** või **Rendi vaatamine** ja valige seejärel **Kasutajate käsitsi määramine/välistamine**.
3. Valige kasutaja, kes rollile määrata ja valige seejärel käsk **Määra rollile**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
