---
title: "Makseviisid kõnekeskuses"
description: "Selles teemas käsitletakse erinevaid makseviise, mida saate Dynamics 365 for Retaili kõnekeskuses kasutada."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 93cff4454139524911a98fc28bccd6aeb5b49d4a
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="payment-methods-in-a-call-center"></a>Makseviisid kõnekeskuses

[!include[banner](includes/banner.md)]


Selles teemas käsitletakse erinevaid makseviise, mida saate Dynamics 365 for Retaili kõnekeskuses kasutada.

Muudes kanalites kasutatavaid makseviise (nt sularaha, tšekke, krediitkaarte ja kinkekaarte) saab kasutada ka kõnekeskustes. Pärast seda, kui olete seadistanud kõnekeskuse makseviisi, kuvatakse see ühe valikuna jaotises **Maksed** lehel **Müügitellimus** kõigi kõnekeskuse kasutajate puhul. Lisaks saate seadistada kupongid, millega pakkuda allahindlusi klientidele, kes esitavad teie organisatsiooni kõnekeskuse kaudu tellimuse. Kupongid võivad pakkuda fikseeritud summaga allahindlust või allahindlusprotsenti kauba hinnast või kogutellimusest. Näiteks summapõhine kupong võib pakkuda klientidele 75.00-eurost allahindlust, kui nad kulutavad vähemalt 750.00 eurot. On võimalik luua erinevat tüüpi kuponge, seadistada põhi-/alamkuponge ja kopeerida või tühistada kupongi. Kasutage kupongide loomiseks järgmises tabelis olevaid valikuid.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Atribuut**             | Sisestage väljale **Lunastamismäär** kupongi eeldatav lunastamismäär protsendina ja seejärel valige, kas kupong on ühekordselt kasutatav, automaatselt uuesti väljastatav või kliendikohane.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Kehtiv**                 | Sisestage väljadele **Alguskuupäev** ja **Lõpukuupäev** kupongi kehtivuse esimene ja viimane kuupäev.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Kaasa/välista reeglid** | Valige väljadel **Kataloogid** ja **Kaubad**, kas kupongist välistatakse mõni kataloog või kaup. Kui valite **Kaasa** või **Välista**, klõpsake valikut **Seadistus**, valige **Kaasa/välista kataloogid** või **Kaasa/välista tooted** ja sisestage teave kataloogi või kauba kohta. Kui teete neil väljadel valiku **Puudub**, kaasatakse kupongile kõik kataloogid või kaubad.                                                                                                                                                                                                                          |
| **Muud**         | Kui seda kupongi ei saa koos muude allahindlustega kasutada, märkige ruut **Välistav**. Seejärel valige väljalt **Päritolu**, kus kupongi saab kasutada. Kui see kupong on tootja kupong, märkige ruut **Tootja kupong**.                                                                                                                                                                                                                                                                                                                                                                |
| **Tulevane kupong**         | Kui kupong seotakse põhiüksusena teiste kupongidega, märkige ruut **Põhikupong**. Kui see kupong tuleks seostada olemasoleva kupongiga alamkupongina, valige väljalt **Põhikupongi ID** põhikupong. Näiteks võite luua kupongi tulevase kevadkataloogi jaoks. Kõik teised kevadkataloogi jaoks loodavad kupongid on edaspidi kevadkataloogi kupongi alamkupongid. Alamkupongid võivad sisaldada 20-protsendilist allahindlust uute klientide tellimustele, 10-protsendilist allahindlust uutele kaupadele või 95.00-eurost allahindlust üle 1000.00-eurostele tellimustele. |

Kui edastate krediitkaardimakse lehelt **Müügitellimus** ja saate sõnumi, mis mainib, et kaart ei ole autoriseeritud, saate autoriseerida käsitsi. Võite krediitkaarditehingu autoriseerida, tagasi lükata või uuesti esitada, kasutades lehte **Autoriseerimise haldamine**. Kõnekeskuse parameetrite lehel saate konfigureerida täiendavaid makse töötlemise valikuid.

-   Tšeki ootelolekud võimaldavad finantsosakonna töötajatel töödelda ootele pandud tellimusi, kuna makseviisina kasutati tšekki ja tšeki ooteloleku lävesumma ületati. Ooteloleku saab käsitsi vabastada või see aegub automaatselt konfigureeritud perioodi lõpus.
-   Saate seadistada läved, mille ületamisel tuleb tšekkide ja krediitkaartide kaudu väljastatud tagasimakseid käsitsi kinnitada. Kõik lävisummat ületavad tagasimaksed lisatakse kinnitusjärjekorda. Pärast tagasimakse kinnitamist saab müügi tagastustellimust arveldada.





