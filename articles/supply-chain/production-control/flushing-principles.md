---
title: Automaatse tarbimise põhimõtted
description: See artikkel kirjeldab nelja tarbimispõhimõtteid, mida kasutatakse toormaterjali tarbimises.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 89fd38ea6d2c1635e9d8974ab99c2e4cdae4d6be
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266424"
---
# <a name="flushing-principles"></a>Automaatse tarbimise põhimõtted

[!include [banner](../includes/banner.md)]

Automaatse tarbimise põhimõtted kajastavad erinevaid tarbimisstrateegiaid tootmisprotsessides kasutatavate toormaterjalide puhul. Tarbimine on protsess, mis lahutab materjali vabast kaubavarust ning seab tootmistellimuste ja partiitellimuste puhul tarbitud materjalide väärtuseks **Pooleliolev töö** (WIP). Toormaterjale tarbitakse tavaliselt asukohast, mis on konfigureeritud materjali tarbivale protsessile. Seda asukohta nimetatakse tootmise sisendasukohaks.

Enne materjali tarbimist teisaldatakse materjalid sisendasukohta. Järgmine illustratsioon näitab seda protsessi.

[![stsenaarium4a.](./media/scenario4a.png)](./media/scenario4a.png)

1. Materjaliladu
2. Toormaterjalide komplekteerimine
3. Toodangu sisendasukoht
4. Toormaterjali tarbimine
5. Tootmisprotsess

Materjali tarbimist juhitakse järgmise nelja automaatse tarbimise põhimõttega.

- Käsitsi
- Käivita
- Valmis
- Asukohas saadaval

Automaatse tarbimise põhimõtted on konfigureeritud vaikeväärtuste hierarhias. Hierarhia algab vabastatud tootega ja automaatse tarbimise põhimõtte väärtus on **Algus**. Koosluse- või valemireal saab tootest pärit automaatse tarbimise põhimõtte tühistada. Automaatse tarbimise vaikepõhimõte tootmise koosluseridadel või partiitellimuse valemiridadel võetakse tootelt või tühistatud väärtusest koosluses või valemites.

## <a name="description-of-the-flushing-principles"></a>Automaatse tarbimise põhimõtete kirjeldus

### <a name="manual"></a>Käsitsi
Käsitsi automaatse tarbimise põhimõte näitab, et materjali tarbimise registreerimine toimub käsitsi. See põhimõte on sobiv näiteks siis, kui soovite jälgida aega ning jälgimiseks tuleb arvesse võtta tarbitud partiide numbrite või seerianumbrite kogust. Käsitsi tarbimine registreeritakse tootmise komplekteerimislehe töölehel. Kaupadele, mis on lubatud laohaldusprotsessidele (WMS), saab rakendada käsikäivitusvoogu.

### <a name="start"></a>Käivita
Automaatse tarbimise põhimõte Algus näitab, et materjali tarbitakse tootmistellimuse käivitamisel automaatselt. Tarbitud materjali kogus on alguskoguse suhtes proportsionaalne. Kui automaatse tarbimise põhimõtet Algus kasutatakse koos tootmise käivitussüsteemiga, saab seda kasutada ka materjalide automaatseks tarbimiseks toimingu või protsessitöö käivitamisel. See põhimõtte on asjakohane, kui näiteks tarbimise hälve on väike, materjalid väheväärtuslikud, jälgimisnõudeid pole või on toimingutel lühike käitusaeg. 

### <a name="finish"></a>Valmis
Automaatse tarbimise põhimõte Lõpp näitab, et materjali tarbitakse automaatselt, kui tootmistellimus teatatakse lõpetatuks või kui materjale tarbima seadistatud toiming registreeritakse lõpule viiduks. Tarbitud materjali kogus on lõpetatuna teatatud koguse suhtes proportsionaalne. Kui automaatse tarbimise põhimõtet Lõpp kasutatakse koos tootmise käivitussüsteemiga, saab seda kasutada ka materjalide automaatseks tarbimiseks toimingu või protsessitöö lõpetamisel. See põhimõte on asjakohane samades olukordades mis põhimõte Algus. Põhimõte Lõpp on siiski mõeldud pikema käitusajaga toimingutele, kus materjalid ei tule seada olekusse WIP, enne kui toiming viiakse lõpule.

> [!NOTE]
> Te ei saa kasutada valikut Lõpeta tühjendamine koos kaupade planeerimisega. Selle asemel soovitame kasutada automaatse kasutamise põhimõtet. Plaanitavatel kaupadel on tootmistüüp *Plaanimisüksus* ning ainult kaastoodete ja kaastoodete puhul saab kaupade planeerimiseks loodud partiitellimuste puhul teatada lõpetatuna.

### <a name="available-at-location"></a>Asukohas saadaval
Automaatse tarbimise põhimõte Saadaval asukohas näitab, et materjali tarbitakse automaatselt, kui see registreeritakse tootmiseks komplekteerituna. Materjal registreeritakse asukohast komplekteerituks, kui töö toormaterjali komplekteerimiseks on lõpule viidud või kui materjal on saadaval tootmise sisendasukohas ja materjalirida on lattu vabastatud. Protsessi käigus loodud komplekteerimisleht sisestatakse pakett-tööna. See põhimõte on asjakohane näiteks juhul, kui teil on ühe tootmistellimusega seotud palju komplekteerimistegevusi. Sel juhul ei pea te komplekteerimislehte käsitsi värskendama ja saate WIP-saldost ajakohase ülevaate.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
