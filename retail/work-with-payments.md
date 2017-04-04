---
title: "Kõnekeskuse makseviisid"
description: "Selles teemas käsitletakse erinevaid makseviise, mida saate jaemüügi ja kaubanduse mooduli kõnekeskuses kasutada."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 636d83ecc7732a164924352853603588cded0db4
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods-in-a-call-center"></a>Kõnekeskuse makseviisid

Selles teemas käsitletakse erinevaid makseviise, mida saate jaemüügi ja kaubanduse mooduli kõnekeskuses kasutada.

Microsoft Dynamics AX-i mooduli Jaemüük ja kaubandus muudes kanalites kasutatavaid makseviise, nt sularaha, tšekke, krediitkaarte ja kinkekaarte, saab kasutada ka kõnekeskustes. Pärast seda, kui olete seadistanud kõnekeskuse makseviisi, kuvatakse see ühe valikuna jaotises **Maksed** lehel **Müügitellimus** kõigi kõnekeskuse kasutajate puhul. Lisaks saate seadistada kupongid, millega pakkuda allahindlusi klientidele, kes esitavad teie organisatsiooni kõnekeskuse kaudu tellimuse. Kupongid võivad pakkuda fikseeritud summaga allahindlust või allahindlusprotsenti kauba hinnast või kogutellimusest. Näiteks summapõhine kupong võib pakkuda klientidele 75.00-eurost allahindlust, kui nad kulutavad vähemalt 750.00 eurot. On võimalik luua erinevat tüüpi kuponge, seadistada põhi-/alamkuponge ja kopeerida või tühistada kupongi. Kasutage kupongide loomiseks järgmises tabelis olevaid valikuid.

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



