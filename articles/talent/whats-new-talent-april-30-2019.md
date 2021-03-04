---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (30. aprill, 2019)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2539baba84bffeb21d351cc307191eea3e940515
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528191"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (30. aprill, 2019)?

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Selles jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2270. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Tagasiside andmine

Talenti tagasiside andmise suvand asub menüüs **Spikker** (**?**). See menüü võimaldab juurdepääsu järgmistele ressurssidele.

- Tagasiside
- Spikker
- Alustamine
- Tugi
- Ideed
- Teave

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Kasutajaliidesele täiustused töötajate duplikaatide tuvastamiseks

Selle muudatuse tõttu tuvastatakse nüüd duplikaadid, kui seate nimeväljad, ja oleku indikaator näitab tuvastatud duplikaatide arvu. Esitatud link avab lehekülje, kus saate hinnata, kas peaksite kasutama ühte duplikaatidest. Andmesisestuse katkestamise vältimiseks ei avane duplikaatide vorm automaatselt. Lehe avamiseks peate valima lingi.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service'i üksuse tugi kohandatud väljadele

Selle nädala väljaandes toetavad järgmised üksused nüüd kohandatud välju: tööhõive, soodustuse tüüp ja palgatsükkel.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Tõrge ilmneb, kui kontroll-loend on määratud (299877)

See muudatus parandab tõrketeadet, mis kuvatakse, kui määrate töötajale kontroll-loendi väljaspool töösuhte lõpetamisprotsessi.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Lahkunud töötajate link avab vale töötaja (309939)

See muudatus lahendab probleemi, mis ilmneb siis, kui olete töötaja teises juriidilise isiku juurest uuesti palganud ja üritate minna töötajavormile lahkunud töötajate loendi kaudu.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Töötaja iseteeninduse kompensatsiooni kaart ei näita koondväärtusi, kui täpsemad turvasätted on sisse lülitatud (315231)

See muudatus parandab probleemi, mis ilmneb, kui kasutate täpsemat hüvitusturvet. Kui täiustatud turvasätted on sisse lülitatud, kuvatakse töötaja iseteeninduses koondtasusummad nii töötajate kui ka juhtide puhul. Enne seda muutust ilmnusid kokkuvõtlikud väärtused kui 0 (null).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Kui ametikohata ametikoht on loodud Common Data Service'is, siis ei looda Talentis ametikohta (314562).

Selle nädala muudatused parandavad probleemi, mis ilmneb siis, kui loote Common Data Service'is ametikohti, kuid ei lisa ametinimetust.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Tõrketeade jõudluse töölehe sisestustes töötaja iseteeninduses (314134)

See muudatus parandab probleemi, mis ilmneb siis, kui lisate jõudluse eesmärgid jõudluse töölehe sisestustele töötaja iseteeninduses.

## <a name="in-preview"></a>Eelvaates

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Puhkuse tüüpidele põhjusekoodide määramise lubamine

Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Nüüd saate määrata puhkuse tüüpidega seotud põhjusekoodid ja lasta töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kindlat tüüpi puhkusetüüpidele ja puhkuseavaldustele põhjusekoodide nõudmine

Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkusetaotluste põhjusekoodide määramist. See nõue võib eksisteerida ettevõtte poliitika või regulatiivsete nõuete tõttu. Nüüd saate määrata, milline puhkusetüüp vajab põhjusekoodi ja saate nõuda, et töötajad esitavad oma puhkuseavaldusel oma puhkusetüübile põhjusekoodi.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine

Võimalus jägida töötaja puhkuseaega ja mõista, kuidas puhkus on arvestatud, mitte ainult ei aita personaliosakonnal (HR) vastata töötajate küsimustele, vaid võimaldab ka töötajatele tagada täpse puhkusehüvitise. Personaliosakonnal on nüüd uus tehingute vaade (hüvitused, viitvõlad, korrigeerimised ja taotlused), et personaliosakond näeks saldode taga olevaid põhjuseid.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="email-support-for-alerts"></a>E-posti tugi teatistele

Finance and Operations platvormi värskendusega 26 saavad kasutajad luua teavituse reegleid, mis saadavad kontaktidele automaatselt sündmuse käivitatud meiliteateid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]