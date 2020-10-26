---
title: Tagastatud kauba sissetuleku registreerimine
description: Võite registreerida tagastatud kaupade sissetuleku, kasutades saabumise ülevaate vormi või registreerimisvormi.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42ca1d4d2d9b45d79cf479833f83e498e3b73540
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975628"
---
# <a name="register-the-receipt-of-returned-items"></a>Tagastatud kauba sissetuleku registreerimine 

[!include [banner](../includes/banner.md)]


Tagastatud kaupade sissetuleku registreerimiseks on kaks meetodi. Esimene meetod on lao kättesaamisprotsess, mis kasutab vormi **Saabumise ülevaade**. Teine kasutab vormi **Registreerimine**.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Tagastatud kaupade saatelehe registreerimine saabumise ülevaate vormis

Saate kasutada vormi **Saabumise ülevaade**, et tuvastada tagastussaadetis selle tagastatud kauba (RMA) koodi järgi. Kui töölehe nimi on määratletud vahekaardil **Seadistamine** ja on olemas töölehe read, mis vastavad vormis **Saabumise ülevaade** valitud ridadele, luuakse uus töölehe päis, kui klõpsate nuppu **Alusta saabumistöölehte**.

1.  Klõpsake valikuid **Varud** \> **Perioodiline** \> **Saabumisülevaade**.

2.  Valige väljas **Seadistuse nimi** suvand **Tagastustellimus** ja klõpsake käsku **Värskenda**.
    

    > [!TIP]
    > <P>Saate otsingutulemuste täpsustamiseks kasutada välju <STRONG>Vahemik</STRONG>. Täpse tulemuse saamiseks saate tippida või valida tagastuskoodi väljal <STRONG>RMA number</STRONG>. Selliste filtrite kogumi määratlemiseks ja salvestamiseks, mis määravad, milliseid sissetulevaid saabumisi kuvatakse, klõpsake vahekaarti <STRONG>Seadistamine</STRONG>. Saadaolevad filtrid sisaldavad tüüpe, ladusid ja alasid.</P>

    

    > [!WARNING]
    > <P>Tagastustellimusi ei saa segada muude saabumise tüüpidega vormis <STRONG>Saabumise ülevaade</STRONG>. Seetõttu on viide alati müügitellimus, kuid ühtki müügitellimuse ID-d ei määrata töölehe päises.</P>



3.  Leidke ruudustikus **Kviitungid** rida, mis sobib tagastatava kaubaga, ja märkige seejärel ruut veerus **Vali saabumise jaoks**.

4.  Selleks et tagastatud sissetulekust välistada kindlad read, nt algse tellimuse kaubad, mida tagastatud saadetises ei olnud, tühjendage nendega seotud märkeruudud **Vali saabumise jaoks** vormi alumisel osal olevas tabelis **Read**.

5.  Klõpsake nuppu **Alusta saabumistöölehte** saabumise töölehe loomiseks.
    

    > [!NOTE]
    > <P>Saate valida mitu tagastustellimust ja kaasata need kõik ühte saabumisprotsessi. Kõik tagastustellimuse read kopeeritakse kauba saabumistöölehe vastavatele ridadele.</P>

    

    > [!NOTE]
    > <P>Samuti saate käsitsi luua saabumistöölehte, kasutades vormi <STRONG>Kauba saabumine</STRONG>. 



6.  Klõpsake valikuid **Laohaldus** \> **Töölehed** \> **Kauba saabumine** \> **Kauba saabumine**.

7.  Valige värskelt loodud saabumistööleht ja klõpsake nuppu **Read**, et avada vorm **Töölehe read, asukohad**.

8.  Vahekaardil **Üldine** kohandage numbrit väljal **Kogus**, kui see on nõutav, ja määrake seejärel likvideerimiskood väljal **Likvideerimiskood**.
    
    Teise võimalusena saate märkida ruudu **Vahelao haldus**, et tagastatud kaubad läbiksid kontrollimisprotsessi vahelaoorderi kontekstis.
    

    > [!NOTE]
    > <P>Kui saadate tagastatud kaubad vahelao kaudu, ei saa likvideerimiskoode määrata.</P>



9.  Klõpsake nuppu **Kontrolli**.

10. Kui kinnitamise protsessis tõrkeid ei esine, klõpsake käsku **Postita**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Tagastatud kaupade saatelehe registreerimine registreerimisvormis

Vormi **Saabumise ülevaade** kasutamise alternatiivina võite kasutada vormi **Registreerimine**, et registreerida tagastatud kaupade saabumine.

1.  Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**. Looge uus tagastustellimus või avage loendist tagastustellimus. Kiirkaardil **Read** valige tagastustellimuse rida. Klõpsake käsku **Värskenda rida** ja seejärel valikut **Registreerimine**.

2.  Määrake likvideerimiskood väljal **Likvideerimiskood** ja klõpsake seejärel nuppu **OK**.
    

    > [!NOTE]
    > <P>Ei ole võimalik saata kaupa kontrollimiseks vahelaoorderina, kasutades vormi <STRONG>Registreerimine</STRONG>.</P>



3.  Ruudustikus **Kanded** valige registreeritav kanne.

4.  Klõpsake ruudustikus **Registreeri kohe** käsku **Lisa**. Korrake kahte eelmist etappi, kuni kõik tagastatud kaubad kuvatakse ruudustikus **Registreeri kohe**.

5.  Klõpsake käsku **Postita kõik**.

## <a name="see-also"></a>Vt ka

[Saabumise ülevaade (vorm)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  


