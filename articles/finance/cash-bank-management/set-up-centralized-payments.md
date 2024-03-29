---
title: Tsentraliseeritud maksete seadistamine
description: Järgige neid juhiseid, et ühes juriidilises isikus teiste organisatsiooni juriidiliste isikute nimel protsessimaksed ette valmistada.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16548572cd70129efcc7dacf0236f3eb4b252d88
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804043"
---
# <a name="set-up-centralized-payments"></a>Tsentraliseeritud maksete seadistamine

[!include [banner](../includes/banner.md)]

Järgige neid juhiseid, et ühes juriidilises isikus teiste organisatsiooni juriidiliste isikute nimel protsessimaksed ette valmistada. Enne alustamist tuleb järgmine seadistus lõpule viia.

-   Juriidiliste isikute loomine.
-   Pearaamatu parameetrite ja kontoplaanide seadistamine.
-   Ostureskontro ja müügireskontro parameetrite seadistamine (olenevalt tsentraliseeritud makseid kasutavatest moodulitest).
-   Kontsernisisese raamatupidamise seadistamine.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Organisatsiooni hierarhia seadistamine tsentraliseeritud maksetele
Peate seadistama organisatsiooni hierarhia tsentraliseeritud maksetele. Sama organisatsiooni hierarhiat kasutatakse tsentraliseeritud tarnijamaksete ja tsentraliseeritud kliendimaksete töötlemiseks. 

>[!Note] 
>Tsentraliseeritud maksete puhul pole hierarhia struktuur oluline. Mis tahes hierarhia juriidiline isik saab hierarhias mõne muu juriidilise isiku nimel makseid töödelda. Lehel **Organisatsiooni hierarhiad** saate luua uue organisatsiooni hierarhia. Väljalt **Eesmärk** tuleb valida **Tsentraliseeritud maksed**. 

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
