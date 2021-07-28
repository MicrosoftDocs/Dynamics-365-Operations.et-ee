---
title: Server-serveri autentimine ATS-integratsiooni API jaoks
description: See teema kirjeldab, kuidas seadistada server-serveri autentimist integratsioonide jaoks Dynamics 365 Human Resources Applicant Tracking System (ATS) integratsiooni API-ga.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ed76d22ab6b917c931220f3ba462f4f14cae207
ms.sourcegitcommit: bd684c9eb6de718573e6be5479e1832fe614d919
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6373057"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Server-serveri autentimine ATS-integratsiooni API jaoks

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema kirjeldab, kuidas seadistada server-serveri autentimist integratsiooniga vastu Dynamics 365 Human Resources Applicant Tracking System (ATS) integratsiooni API-ga. Virtuaaltabelile ja seotud andmetele juurdepääsuks on vaja teenuse subjekti jaoks hallata teatud Microsoft Dataverse turvakihte. Kasutajale peab olema antud juurdepääs Dataverse virtuaaltabelile rakenduses Microsoft Power Platform ja juurdepääsu Dynamics 365 Human Resources andmetele.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Luba juurdepääs virtuaalsetele Dataverse tabelitele rakendduses Power Platform

Esimene etapp, mis võimaldab juurdepääsu Dataverse virtuaaltabelitele Power Platform rakenduses, , on seadistatud Power Platform autentimiseks virtuaaltabeli Dataverse lõpp-punktide suhtes. Selle tegemise etapid on kirjeldatud [Microsoft Dataverse arendaja juhnedis](/powerapps/developer/data-platform).

  - Ühe rentniku rakenduse registreerimiseks: [kasutage ühe rentniku serverilt serverile autentimist](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Mitme rentniku rakenduse registreerimiseks: [kasutage mitme rentniku serverilt serverile autentimist](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>ATS-integratsioonide turberolli loomine

Üks pärast rakenduse kasutaja loomist on määrata kasutaja turberollile, mis määratleb rakenduse juurdepääsu lõpp-punktidele. See on etapp 7 [rakenduse kasutaja loomises](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) ühe rentniku rakenduse registreerimistele ja [looge rakenduse kasutajale turberoll](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) mitme rentnikuga registreerimiste jaoks. 

Rollil, millele määrate rakenduse kasutaja, peaks olema juurdepääs teie ATS-i integreerimiseks kasutatavatele andmeüksustele. See puudub ruudust väljas, seega tuleb luua uus turberoll. Uue rolli saab luua vastavalt jaotises kirjeldatud juhistele [Turberolli loomine](/power-platform/admin/create-edit-security-role#create-a-security-role).

Uue rolli jaoks tuleb uue rolli vahekaardil **Kohandatud üksused** määrata vähemalt järgmistele üksustele sobiv juurdepääs. Arvestage, et võib olla lisaüksuseid, mida peate võib-olla lisama, kui integratsioon kasutab rohkem rakenduse andmeid. Pärast uue rolli loomist saab selle rakenduse määrata kasutajale.

  - Põhitöötaja (mshr)
  - Palgatava kandidaat (mshr)
  - Kompetentsi sert (mshr)
  - Serdi tüüp (mshr)
  - Ettevõte
  - Hüvitatud töö funktsioon (mshr)
  - Hüvitatud töö tüüp (mshr)
  - Riik/regioonid (mshr)
  - Osakond (mshr)
  - Hariduse kompetents (mshr)
  - Hariduskraad (mshr)
  - Hariduse distsipliin (mshr)
  - Haridusnõuded (mshr)
  - Identifitseerimine (mshr)
  - Identifitseerimistüüp (mshr)
  - Asutus (mshr)
  - Väljaandev asutus (mshr)
  - Töö hüvitamine (mshr)
  - Tööd (mshr)
  - Haridustase (mshr)
  - Osapoole kontaktid (mshr)
  - Inimesed (mshr)
  - Isiku aadressid (mshr)
  - Isiku skriining (mshr)
  - Ametikoha tüüp (mshr)
  - Ametikoha V2 (mshr)
  - Töökogemuse kompetents (mshr)
  - Hindamise tase (mshr)
  - Reitingumudelid (mshr)
  - Põhjusekoodid (mshr)
  - Värbamistaotlus (mshr)
  - Värbamistaotluse asukoht (mshr)
  - Värbamistaotluse ametikoht (mshr)
  - Värbamistaotluse oskus (mshr)
  - Skriiningu tüüp (mshr)
  - Oskuste kompetents (mshr)
  - Oskused (mshr)
  - Tiitlid (mshr)
  - Veterani olek (mshr)
  - Töötaja (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Rakenduse õiguste andmine inimressursside andmetele

Teiseks sammuks on tagada, et rakendusele antakse inimressurssides andmete jaoks asjakohane luba, sidudes selle kasutajaga inimressursside rakenduses. Rakenduse kasutaja jaoks tehakse serverilt serverile Dataverse virtuaalsete tabelite kaudu kutseid kasutaja (rakenduse) Dataverse identiteedi kontekstis, mis toimingu käivitab. Virtuaaltabeli adapteri teenus otsib siis seotud kasutaja inimressurssidest ja käivitab päringu selle kasutaja kontekstis. See tähendab, et kasutaja tuleb luua Inimressurssides korrektsete rollidega, mis on määratud juurdepääsuks andmetele, mida integreeriv rakendus vajab.

Inimressursside kasutajale tuleb määrata ka õiged õigused Inimressurssides andmete jaoks. **Värbamistaotluse** (HcmRecruitingIntegrator) roll on saadaval privileegidega esmastele üksustele, mis on vajalikud värbamisandmetega integreerimiseks. Rolli saab määrata rakenduse kasutajale lehel **Kasutajad** et anda andmetele sobiv juurdepääs. Lisateavet inimressursside turberollide kohta vaata [Rollipõhisest turbest](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Uue kasutaja häälestamine koos asjakohaste õigustega

Uue kasutaja häälestamiseks koos asjakohaste õigustega, järgige järgmisi samme:

  1. Avage **Kasutaja** lehekülg inimressurssides ja valige **Uus**.
  2. Sisestage **kasutaja ID** ja **kasutaja nimi** rakenduse uue kasutaja jaoks. Näiteks võite sisestada "Värbamisintegratsioon".

      > [!NOTE]
      > Kui rakendusel ei ole Microsoft`i Azure Active Directory (Azure AD) kasutajakontot või meiliaadressi, saate panna kasutaja meiliaadressile ja pakkuja väljadele näiteks "RecruitingApp".

  3. Kiirkaardil **Kasutaja rollid** valige tegevus **Määra rollid**.
  4. **Kasutajapaanil rollide** määramiseks valige **värbamisrakendus** ja valige **Ok**.
  5. Salvestage uus kasutajakirje.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Uue inimressursside kasutaja linkimine rakendusega

Kui kasutaja on loodud, tuleb rakenduse jaoks luua kirje vormis **Azure Active Directory rakenduse** vorm et linkida rakendus Inimressursside kasutajaga.

  1. Avage vorm **Azure Active Directory rakenduse** vorm ja valige **Uus**.
  2. Sisestage **Kliendi ID** väljale rakenduse jaoks loodud rakenduse kasutaja kliendi ID.
  3. Sisestage väljale **Nimi** integratsioonirakenduse nimi.
  4. Valige **Kasutaja ID** väljale uus inimressursside kasutaja, mis loodi värbamise integreerimiseks.
  5. Salvestage uus kasutajakirje.

Siis on rakendusel juurdepääs inimressursside andmetele, mis on piiratud ainult värbamisrakenduste integratsioonide jaoks vajalike andmetega.

## <a name="see-also"></a>Vt ka

[Kandidaatide värbamine](hr-personnel-recruit.md)<br>
[Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse'i Web API kasutamine](/powerapps/developer/data-platform/webapi/overview)<br>
[Suvandikomplektide loomine ja värskendamine Web API abil](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
