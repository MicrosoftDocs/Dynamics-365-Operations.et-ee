---
title: Hüvitusprotsessi määratlemine ja tulemuste arvutamine
description: Tasuprotsesse kasutatakse uute tasusummade ja preemiate määramiseks põhipalga ja ergutussüsteemi plaanides registreeritud töötajatele.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 188a87f580c274e073710601ef306139f723c797
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071710"
---
# <a name="define-compensation-process-and-calculate-results"></a>Hüvitusprotsessi määratlemine ja tulemuste arvutamine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tasuprotsesse kasutatakse uute tasusummade ja preemiate määramiseks põhipalga ja ergutussüsteemi plaanides registreeritud töötajatele. Tasuprotsessi saab käitada mitu korda, et teha tegurite mõju analüüsi, kontrollimaks, et kõik muudatused ja sätted on õiged. See protseduur loob tasuprotsessi, käitab protsessi ja kuvab tulemused. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-compensation-process"></a>Tasuprotsessi loomine
1. Minge **kompensatsioonihalduse** > **Protsessi** > **kompensatsiooniprotsessidele**.
2. Klõpsake valikul **Uued hüvitusprotsessid**.
3. Sisestage väärtus väljale **Protsess**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige suvand väljal **Protsessi tüüp**.
    * Tsükkel määrab tasu määramiseks hinnatava ajavahemiku. Hindamisel arvestatakse, millistel ametikohtadel töötajad olid, milliseid tulemuste hinnanguid kaasata, ajaprotsendi arvutust, mille jooksul töötaja tsükli ajal töötas jne. Tsükli alguskuupäeva näide võib olla eelmise finantsaasta esimene päev.  
6. Sisestage kuupäev väljale **Tsükli algus**.
    * Tsükli lõppkuupäev on oluline, kuna see on kuupäev, mida kasutatakse määramiseks, millised töötajad aktiivselt töötasid ja registreerusid ühes või mitmes tasuplaanis.  
7. Sisestage kuupäev väljale **Tsükli lõpp**.
    * Kande jõustumise kuupäev on kuupäev, millal uued tasumäärad jõustuma peaksid. Paljud ettevõtted lisavad mõned kuud tsükli lõpu ja uute tasumäärade jõustumisaja vahele. Lisaaega kasutatakse uue tasu töötlemiseks ja ülevaatamiseks.  
8. Sisestage kuupäev väljale **Kande aktiivne kuupäev**.
    * Seda ajahetke kuupäeva kasutatakse ergutussüsteemi plaanide puhul, mis määravad töötaja preemiasumma tema tasumäära põhjal sellel ajahetkel.  
    * Fikseeritud töötasu proportsionaalset rendikuupäeva kasutatakse fikseeritud hüvitiste plaanide puhul, mille rendireegel on **protsenti**. Töötajad, kes palgatakse tsükli alguse ja palkamise kuupäevaga proportsionaalse põhipalga kuupäeva vahel, saavad proportsionaalse protsendi asemel 100% oma arvestuslikust palgatõusust.  
9. Sisestage kuupäev väljale **Fikseeritud palk proportsionaalselt palkamise kuupäevaga**.
    * Ülevaatamise tähtaeg on kuupäev, milleks kõik protsessi tulemused tuleb üle vaadata, et need saaks laadida töötaja tasukirjesse enne kande jõustumise kuupäeva. See väli on üksnes teavituslik.  
10. Sisestage lõpukuupäev väljale **Ülevaatamise tähtaeg**.
11. Klõpsake nuppu **Salvesta**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Looge hüvitamisprotsessi jaoks hüvitise plaanid ja toimingud
1. Klõpsake **Häälestus**.
    * **Seadistamise** lehte kasutatakse valimiseks, milliseid plaane selle tasuprotsessi raames töödelda ja milliseid toiminguid iga plaani puhul teha tuleks.  
2. Sisestage või valige väärtus väljal **Plaan**.
3. Klõpsake nuppu **Salvesta**.
4. Klõpsake käsku **Lisa**.
5. Valige väljal **Toiming** toimingu tüüp **Omakapital**.
6. Klõpsake käsku **Lisa**.
7. Valige väljal **Toiming** toimingu tüüp **Väärtus**.
    * Tasutoimingud saab kokku liita, kasutades välja **Kasuta eelmist tulemust** näitamiseks, kas valitud toiming peaks kasutama selle toimingu arvutuse lähtepunktina töötajate põhipalka või eelmise toimingu tulemust.  
8. Valige **Jah** aastal **Kasuta eelmist tulemust** valdkonnas.
9. Klõpsake käsku **Lisa**.
10. Valige väljal **Toiming** toimingu tüüp **Üldine**.
    * Erinevad tasutoimingute tüübid aktiveerivad erinevad väljad. Üldise tasutoimingu tüübi puhul saab määrata kasvuprotsendi või kasvusumma.  
11. Tehke valik **Vali kasvu summa**.
12. Sisestage number väljale **Kasvu summa**.
13. Klõpsake käsku **Lisa**.
14. Valige väljal **Toiming** toimingu tüüp **Edutamine**.
    * Toimingutüübid Edutamine ja Muu taseme muutus võimaldavad kasutajatel töötaja tasu käsitsi kohandada. Nende toimingutüüpide ja muude toimingutüüpide puhul saab lubada soovitusi, et saaksite sisestada töötajale uue soovitusliku tasuväärtuse.  
15. Klõpsake käsku **Lisa**.
16. Valige suvand väljalt **Tüüp**.
    * Põhipalga ja ergutussüsteemi plaane saab käitada samas tasuprotsessis.  
17. Sisestage või valige väärtus väljal **Plaan**.
    * Kasutage märkeruutu **Luba tulemuspalk** määramiseks, kas põhipalga ja ergutussüsteemi summasid tuleks kohandada töötaja tulemusnäitajate alusel.  
    * Ergutussüsteemi plaanidel saab selle mõju alistada.  
18. Klõpsake nuppu **Salvesta**.
19. Klõpsake käsku **Lisa**.
20. Sulgege leht.

## <a name="run-the-compensation-process"></a>Tasuprotsessi käitamine
1. Klõpsake käsku **Käivita protsess**.
    * Nupp **Töötlemise tulemuste** näitamine võimaldab vaadata kogu tasuprotsessi töötlemissõnumeid, kui töötlemine on lõppenud.  
2. Tehke väljal **Töötlemise tulemuste** näitamine valik **Jah**.
3. Klõpsake valikut **OK**.

## <a name="view-the-results"></a>Tulemuste vaatamine
1. Klõpsake valikut **Protsessi tulemused**.
2. Klõpsake valikut **Töötaja tulemused**.
3. Otsige loendist ja valige soovitud kirje.
4. Laiendage **Fikseeritud hüvitis** osa.
    * Laiendage protsessi tulemuste vaatamiseks kiirkaarte. Kui tasutegevuse puhul märgiti valik **Soovituste lubamine**, lubatakse selle toimingu puhul **soovituse** väljad.  
5. Otsige loendist ja valige soovitud kirje.
    * Ühe töötaja tulemused saab kuvada, klõpsates nuppu **Tulemuste kuvamine**.  
    * Saate arvutatud tasusumma üle kirjutada, kohandades kasvusumma protsenti väljadel **Soovitused**.  
6. Sisestage arv väljale **Soovitatav protsent**.
7. Otsige loendist ja valige soovitud kirje.
8. Sisestage arv väljale **Soovitatav protsent**.
    * Ümberarvutamise abil saab eirata olemasoleva kirje muudatusi ja luua valitud töötajale uue tasutulemuse.  
    * Kui kõik töötaja muudatused on tehtud, määrake olekuks **Kinnitatud**.  
9. Klõpsake valikut **Muuda olekut**.
10. Klõpsake nuppu **Kinnitatud**.
    * Pärast kirje kinnitamist saab selle laadida töötaja ametlikku tasukirjesse. Uus tasu jõustub tasuprotsessis määratud kande kuupäevast.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
