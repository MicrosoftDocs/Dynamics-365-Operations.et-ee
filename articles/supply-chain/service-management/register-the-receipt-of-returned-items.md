---
title: Tagastatud kauba sissetuleku registreerimine
description: Võite registreerida tagastatud kaupade sissetuleku, kasutades saabumise ülevaate vormi või registreerimisvormi.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4942e455350844ac5614e70fef21b37461540a6
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017285"
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

1.  Klõpsake müügi **ja turunduse müügi** \> **tagastused** \> **kõik tagastustellimused**. Looge uus tagastustellimus või avage loendist tagastustellimus. Kiirkaardil **Read** valige tagastustellimuse rida. Klõpsake käsku **Värskenda rida** ja seejärel valikut **Registreerimine**.

2.  Määrake likvideerimiskood väljal **Likvideerimiskood** ja klõpsake seejärel nuppu **OK**.
    

    > [!NOTE]
    > <P>Ei ole võimalik saata kaupa kontrollimiseks vahelaoorderina, kasutades vormi <STRONG>Registreerimine</STRONG>.</P>



3.  Ruudustikus **Kanded** valige registreeritav kanne.

4.  Klõpsake ruudustikus **Registreeri kohe** käsku **Lisa**. Korrake kahte eelmist etappi, kuni kõik tagastatud kaubad kuvatakse ruudustikus **Registreeri kohe**.

5.  Klõpsake käsku **Postita kõik**.

## <a name="see-also"></a>Vt ka

[Saabumise ülevaade (vorm)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]