---
title: Tsentraliseeritud maksete seadistamine
description: "Järgige neid juhiseid, et ühes juriidilises isikus teiste organisatsiooni juriidiliste isikute nimel protsessimaksed ette valmistada."
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 975497e8ed0c9738c225bad4db9165bf2ebc0192
ms.openlocfilehash: 0b33e37699fb9b81ad1803f670a4dedbce6a9c29
ms.contentlocale: et-ee
ms.lasthandoff: 06/05/2017

---

# <a name="set-up-centralized-payments"></a>Tsentraliseeritud maksete seadistamine

[!include[banner](../includes/banner.md)]


Järgige neid juhiseid, et ühes juriidilises isikus teiste organisatsiooni juriidiliste isikute nimel protsessimaksed ette valmistada. Enne alustamist tuleb järgmine seadistus lõpule viia.

-   Juriidiliste isikute loomine.
-   Pearaamatu parameetrite ja kontoplaanide seadistamine.
-   Ostureskontro ja müügireskontro parameetrite seadistamine (olenevalt tsentraliseeritud makseid kasutavatest moodulitest).
-   Kontsernisisese raamatupidamise seadistamine.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Organisatsiooni hierarhia seadistamine tsentraliseeritud maksetele
Peate seadistama organisatsiooni hierarhia tsentraliseeritud maksetele. Sama organisatsiooni hierarhiat kasutatakse tsentraliseeritud tarnijamaksete ja tsentraliseeritud kliendimaksete töötlemiseks. **Märkus.** Tsentraliseeritud maksete puhul pole hierarhia struktuur oluline. Mis tahes hierarhia juriidiline isik saab hierarhias mõne muu juriidilise isiku nimel makseid töödelda. Lehel **Organisatsiooni hierarhiad** saate luua uue organisatsiooni hierarhia. Väljalt **Eesmärk** tuleb valida **Tsentraliseeritud maksed**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Kontsernisisese konto seadistamine tsentraliseeritud makseteks
Kui praeguse juriidilise isiku maksekanded on teiste juriidiliste isikute arvetega tasakaalustatud, luuakse igale juriidilisele isikule sobivad võlakanded. Peate täpsustama juriidilise isiku, kus iga rakenduva skonto ja iga realiseeritud kasumi või kahjumi summad sisestatakse. Enne alustamist otsustage, millist juriidilist isikut hankija ja kliendi maksete töötlemiseks kasutatakse. Kui üks juriidiline isik töötleb hankija makseid, kuid teine juriidiline isik töötleb kliendi makseid, peate igale juriidilisele isikule lülituma. Lehel **Kontserni raamatupidamine** saate valida kontsernisisese seose kirje juriidilisele isikule, kelle nimel makseid töötlete. 

Vahekaardil **Tsentraliseeritud maksed** saate valida, kas sisestada skontod makse juriidilisse isikusse (või mõnda teise kandesse, mis vähendab hankijakonto saldot) või arve juriidilisse isikusse (või mõnda teise kandesse, mis vähendab hankijakonto saldot). See valik toimib koos väljaga **Skonto haldamine** lehtedel **Ostureskontro parameetrid** ja **Müügireskontro parameetrid**. Ülemaksete ja sendierinevuse kõikumise puhul kasutatakse tasakaalustust makse juriidilise isikuga. Alamaksete ja sendierinevuse kõikumise puhul kasutatakse tasakaalustust arve juriidilise isikuga.

## <a name="map-vendor-accounts-across-legal-entities"></a>Hankijakontode vastendamine juriidiliste isikute hulgas
Kui maksate hankijale ühelt juriidiliselt isikult ja soovite valida selle hankija arveid muude juriidiliste isikute puhul, peate veenduma, et iga juriidilise isiku kõik asjakohase hankija kontod kasutavad kõik sama aadressiraamatu ID-d. Kui saate makse kliendilt, kes tasub arveid rohkem kui ühele juriidilisele isikule, peate veenduma, et iga juriidilise isiku kõik asjakohased kliendikontod kasutavad sama aadressiraamatu ID-d.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Seadistage sisestusprofiilid tsentraliseeritud maksetele
Kui loote makse ühele juriidilisele isikule, mis tasakaalustab arveid teistele juriidilistele isikutele, peavad sisestusprofiili ID-d mõlema juriidilise isiku puhul kattuma. Maksete korrektse loomise tagamiseks seadistage igale arveldatavale juriidilisele isikule sisestusprofiil, mis vastab makse juriidilise isikuga kasutatavatele sisestusprofiilidele. Vahetage arve esimesele juriidilise isikule ja seejärel saate lehel **Hankija sisestusreeglid** luua uued sisestusreeglid või redigeerida olemasolevaid sisestusreegleid. Arve juriidilises isikus sisestusreeglitele tehtavad valikud ei pea ühtima makse juriidilises isikus olevate sisestusreeglite seadistusele.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Seadistage makseviisid tsentraliseeritud maksetele
Kui loote makse ühele juriidilisele isikule, mis tasakaalustab arveid teistele juriidilistele isikutele, peavad makseviiside ID-d mõlema juriidilise isiku puhul kattuma. Maksete korrektse loomise tagamiseks seadistage igale arveldatavale juriidilisele isikule makseviis, mis vastab makse juriidilise isikuga kasutatavatele makseviisidele. Minge esimesele arve juriidilisele isikule ja seejärel saate lehel **Makseviisid** luua uue makseviisi või muuta olemasolevat makseviisi. Arve juriidilise isiku makseviisi puhul tehtavad valikud ei pea ühtima makse juriidilise isiku makseviisi seadistusega.

## <a name="set-up-default-descriptions"></a>Vaikekirjelduste seadistamine
Saate määrata vaikekirjeldused kontsernisisestele tasakaalustuskannetele. Vaikekirjeldus kaasatakse kannetele, mis ollakse võlgu või mis on võlgnikult saada ettevõtetevahelise tasakaalustusprotsessi käigus. Lehel **Vaikekirjeldused** saate luua uusi kirjeldusi nii suvandite **Kontsernisisese kliendi tasakaalustus** kui ka **Kontsernisisese hankija tasakaalustus** puhul, valides keele ja sisestades seejärel teksti.




