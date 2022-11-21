---
title: Dynamics 365 Human Resources kliendi migratsioon finantside ja toimingute infrastruktuuri
description: See artikkel kirjeldab Kliendi siirde Microsofti finantside Dynamics 365 Human Resources ja toimingute infrastruktuuri.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760358"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources kliendi migreerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kliendi migratsioon on kliendi andmebaasi "üles- ja vahetuse migratsioon" (liikumine) finantside ja toimingute infrastruktuuri. Jaoks kasutatakse automaatset migreerimistööriista. Tulemuseks on uus finants- ja toimingute keskkond, mis kasutab kliendi Inimressursside andmebaasi.

## <a name="prerequisites"></a>Eeltingimused

### <a name="user-access-and-permissions"></a>Kasutaja juurdepääs ja õigused

- Elutsükli Microsoft Dynamics teenuste kasutajal peaks olema organisatsiooni **halduse** roll.
- Kasutaja saab luua projekte või [Azure DevOps kasutada](/azure/devops/organizations/projects/create-project) olemasolevat Azure DevOps projekti.
- Kasutajal peab olema juurdepääs [isikliku juurdepääsu Azure DevOps turvalisuse loa](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) loomiseks või peab kasutajal olema kasutamiseks luba.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse keskkonna varundamine (Box)

 - Valikuline, kuid soovitatav: värskendage olemasolevat inimressursside sisendkausta keskkonda, kasutades inimressursside tootmiskeskkonna koopiat.
 - Looge halduskeskust Dataverse kasutades Power Platform uus keskkond.
 - Kopeerige Dataverse olemasolev keskkond, mis on lingitud eraldi rakendusega Inimressursid, keskkonnas, mille lõite eelmises sammus.

> [!NOTE]
> Andmebaasi lisamisel veenduge, et suvandi **Luba Dynamics 365 rakendused väärtuseks** on seatud **Jah**. Lisateavet vt keskkonna [ettevalmistamine Power Platform](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse Võimsuse

1. Kasutage halduskeskuse **lehekülge** Kokkuvõte Power Platform veendumaks, et ladustamisel [Dataverse](/power-platform/admin/finance-operations-storage-capacity) on keskkonnakoopia jaoks piisavalt vaba võimsust.
2. Kui saadaolevat võimsust pole piisavalt, [kasutage juhiseid ladustamisruumi vabastamiseks](/power-platform/admin/free-storage-space), et kogu tarbimist vähendada. Kliendid saavad lisada [ka täiendavat ladustamisvõimsust](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Kliendi migreerimisprotsess

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Töötsükli teenuste projekti loomine inimressursside migreerimiseks

Esimene samm on luua uus finantside ja toimingute rakendusprojekt elutsükli teenustes. Kliendil on olemasolev inimressursside elutsükli teenuste projekt. Olemasolevad inimressursside keskkonnad migreeritakse uude finantside ja toimingute rakendusprojekti.

Uue projekti loomiseks järgige neid samme.

1. Logige elutsükli teenustesse sisse globaalse administraatorina või teenusekonto määratud kasutajana.
2. Elutsükli teenuste avalehel valige käsk **Loo/uus (+).**.
3. Valige tootena finantside ja toimingute rakendused.
4. **Väljal Projekti eesmärk** valige suvand **Rakendamine**.
5. Sisestage projekti nimi ja kirjeldus.
6. Valige projekti **kohandatud tüübi** väljal Microsofti **Dynamics 365 Human Resources migratsioon**.
7. Valige märkeruut, et tingimustega nõustuda.
8. Valige **Loo**.

Pärast uue elutsükli teenuste projekti loomist järgige selle häälestamiseks ja konfigureerimiseks neid samme.

1. Projekti **lõpuleviimiseks ja projekti** lõpuleviimiseks valige suvand Projekt on soovitud. Lisateavet vt "Projektiletamine ["](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Valige praeguse keskkonnaga sama piirkond. See valik ei mõjuta siirdeid.
    - Pärandsüsteemide puhul valige **muu**.

2. Viige projekti sätted lõpule. Osana sellest sammust peaksite konfigureerima SharePoint Online teek ja Azure DevOps Azure’i ühendused, kui neid vaja. Lisateavet vt elutsükli [teenuste (LCS) kasutusjuhendist](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Kliendid saavad kasutada olemasolevat projekti Azure DevOps ja sellega seotud isikliku juurdepääsu turvalisuse luba. Olemasoleva projekti kasutamisel on projektiga seotud konfiguratsioonid automaatselt saadaval ja neid saab täpsuse üle vaadata.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Inimressursside kausta keskkonna migreerimine

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Selles kaustas keskkonna migreerimiseks valmistumine

Kui uus elutsükli teenuste projekt on loodud ja projekti sisseostmise protsess on lõpetatud, olete valmis oma esimest keskkonda üle siirdama. Enne selle protsessi käivitamist soovitame uuendada sisendkausta keskkonda, mida soovite oma tootmiskeskkonnast eraldi infrastruktuuri üle võtta.

#### <a name="prepare-a-power-platform-environment"></a>Power Platform Keskkonna ettevalmistamine

> [!NOTE]
> See samm on rakendatav ainult sisendkausta keskkonna migreerimise puhul. Kui kannate tootmiskeskkonda üle, Power Platform edastatakse tootmiskeskkonnaga seotud olemasolev halduskeskuse keskkond. Andmebaasi lisamisel veenduge, et nupp **Luba Dynamics 365 rakendused oleks** seatud väärtusele **Jah**. 

- Looge Power-platvormi halduskeskuses keskkond koos [andmebaasiga, mida](/power-platform/admin/create-environment#create-an-environment-with-a-database) kasutada kaustade siirdamiseks, või valige olemasolev keskkond.
- [Kopeerige keskkond](/power-platform/admin/copy-environment) vastendamiseks Power Platform kasutatava keskkonna värskendamiseks.

#### <a name="migrate-the-sandbox-environment"></a>Kanna üle kohtamuutuv keskkond

1. Logige elutsükli teenustesse sisse globaalse administraatorina või teenusekonto määratud kasutajana.

    > [!NOTE]
    > Soovitame kasutada nimelise kasutajakontot. Sisse logitud kasutajal peaks olema projekti **omaniku** **või keskkonnahalduri** turberoll eraldi inimressursside elutsükli teenuste projektis.

2. Avage vastloodud inimressursside migratsiooniprojekt.
3. Vaadake läbi ja viige lõpule migratsioonimetoodika ja projektiga seotud etapid.
4. Valige projekti armatuurlauda vaikespaanil **Standardne aktsepteerimise testpaan** **suvand Kanna hr-i üle**.
5. Paani **ülekandmiseks** valige keskkonnas Vali ülekandmiseks sobiv elutsükli teenuste projekt ja algne inimressursside keskkond (allikast eraldiseisev inimressursside rakendus).
6. Lubage **vastendamine uue Power Platform keskkonnaga** ja valige sobiv Power Platform keskkond. Seejärel valige **Järgmine**.
7. Viige üksikasjade **ja kliendi välja logimise kinnitamiseks lõpule juurutamise sätete (finantsid ja toimingud –** toimingukaad) viisard ning valige käsk **Juuruta**.

Keskkonna olek näitab edenemist. Olek muudetakse olekust Laadimine olekusse **Juurutatud** **·**.**·**

> [!NOTE]
> Tootmispaan pole saadaval enne, kui projekti reaalajas valmisoleku kontroll-loend on lõpule viidud. Lisateavet vt "Reaalajas [ettevalmistamine"](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Kaalutlused ja eeldused

Inimressursside sisendkausta keskkond on elutsükli teenuste projektis rentnikul, mille omadused on järgmised:

- Inimressursside kausta keskkond pole olemasoleva ühendatud keskkonnaga lingitud. Antud inimressursside keskkonnas saab korraga olla pooleli ainult üks migratsioon.
- Ajal lubatud päevakaudu keskkondade arv põhineb inimressursside litsentsil. Kui rentniku jaoks on ostetud piisavalt litsentsi, loetletakse projekti paanil **Keskkonnad** kasti täiendavad boksikeskkonnad.
- Migreerimine tuleb teha sama tüüpi keskkondades. See tähendab, et teha saab ainult kaustast tootmisse või tootmisse siirdamist.

    > [!NOTE]
    > Tootmise või boksi oleku määramisel kaalutakse ainult inimressursside keskkonna tüüpe. Kui keskkonnad on valesti kategoriseeritud (st tootmiskeskkond on märgitud kastikeskkonnana või on sisendkausta keskkond märgitud tootmiskeskkonnaks), pöörduge tugiteenuste poole.

- Kui siirde nurjumine ei õnnestunud, kuvatakse tõrketeade ja nupp **Kustuta** muutub kättesaadavaks. Kasutage seda nuppu nurjunud migreerimise kustutamiseks. Seejärel saate keskkond uuesti migratsioonida.

#### <a name="validate-the-sandbox-migration"></a>Kinnitageboxi migreerimine

Pärast siirdeprotsessi edukat lõpetamist looge üksikasjalik testimisplaan kõigi äriprotsesside kontrollimiseks ja välja logimiseks.

Enne testimise alustamist kontrollige järgmisi üksikasju.

- Veenduge, et ülekantud keskkond oleks loodud URL-il juurdepääsetav.
- Veenduge, et kasutajatel oleks juurdepääs migreeritud boksile.
- Veenduge, et Dataverse migreeritud kaustakeskkonnaga seostatud keskkonnale oleks juurdepääs.
- Puduge erinevaid andmeid kontrollimaks, et saadaval on kõige ajakohasemad andmed.
- Kriitilise tähtsusega äriprotsesside kinnitamine
- Kinnitage, et teie turbepoliitikad on rakendatavad.
- Kinnitage, et pakett-tööd käivitatakse nii, nagu oodatud.

Teil pole kaugtöölaua juurdepääsu migreeritud boksile. Saate kasutada iseteeninduse võimalusi ja tööriistu järgmiste tegevuste sooritamiseks oma järgu 2+ sisendkausta keskkondades:

- Pääsete juurde [Azure SQL-andmebaasile](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Pääsete [juurde logifailidele](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Kasutage [perfmoni tööriistu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Lülitage [hooldusrežiim sisse/välja](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Taaskäivita [teenused](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Regression [suite’i automatiseerimistööriista konfigureerimine](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Lisateavet vt KKK-st [iseteeninduse juurutuse kohta](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Inimressursside tootmiskeskkonna migreerimine

Pärast seda, kui olete kaustakeskkonna migreerimise ja kinnitamise lõpetanud, järgige tootmiskeskkonna migreerimiseks neid samme.

#### <a name="prerequisites"></a>Eeltingimused

- Kordustellimuse algataja peab olema lõpule viidud.
- Go-live’i [valmisoleku hindamine](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) tuleks lõpule viia.

#### <a name="migrate-the-production-environment"></a>Kanna tootmiskeskkonda üle

1. Logige elutsükli teenustesse sisse globaalse administraatorina või teenusekonto määratud kasutajana.

    > [!NOTE]
    > Soovitame kasutada nimelise kasutajakontot. Sisse logitud kasutajal peaks elutsükli **teenuste** projektis **olema** projekti omaniku või keskkonnahalduri turberoll.

2. Avage uus inimressursside siirde projekt.
3. Vaadake läbi ja viige lõpule migratsioonimetoodika ja projekti asjakohased faasid.
4. Valige projekti armatuurlaud paanil **Tootmine** suvand Kanna inimressursside üle.**·**
5. Valige paani **ülekandmiseks** keskkonnas Vali keskkond, valige sobiv elutsükli teenuste projekt ja algne inimressursside keskkond (allikast eraldiseisev inimressursside rakendus). Seejärel valige **Järgmine**.
6. Viige üksikasjade **ja kliendi välja logimise kinnitamiseks lõpule juurutamise sätete (finantsid ja toimingud –** toimingukaad) viisard ning valige käsk **Juuruta**.

Keskkonna olek näitab juurutamise edenemist. Olek muudetakse olekust Laadimine olekusse **Juurutatud** **·**.**·**

#### <a name="post-migration-considerations"></a>Migreerimise järgsed kaalutlused

- Rakendage oma [keskkondades](/fin-ops-core/fin-ops/get-started/quality-updates) viimased kvaliteediuuendused.
- Virtuaaltabelite kasutamisel [konfigureerige](hr-admin-integration-common-data-service-virtual-entities.md) lõpp-punktid ümber.
- Konfigureerige ümber topeltkirjutuse integreerimine. Hindage, millised üksused peavad olema lubatud.
- Kaaluge virtuaaltabelite kasutamist topeltkirjutuse asendamiseks integratsiooni jaoks.

#### <a name="dual-write-integration"></a>Topeltkirjutuse integratsioon

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Saate häälestada topeltkirjutuse Microsoft Power Platform integratsiooni.

1. Minge halduskeskuse Power Platform ja valige vasakpoolsel **navigeerimisel** keskkonnad.
2. Valige eelnevalt kopeeritud/värskendatud keskkond ja kinnitage, et olek on **Valmis**.
3. Minge elutsükli teenustesse ja kinnitage, et migreerimisprojekti olek on **Juurutatud**.
4. Ülekantud keskkonnas valige täielikud üksikasjad **täiendavate** üksikasjade ülevaatamiseks ja [topeltkirjutuse rakenduse häälestamiseks](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Topeltkirjutuse rakenduse konfiguratsioonipaanil **märkige ruut, et nõustuda andmete vastendamise ja sünkroonimisega andmebaaside vahel ning seejärel valige suvand Konfigureeri** **.**
6. Kui teateboks teavitab teid edukast topeltkirjutuse konfiguratsioonist, valige **OK**.
7. Saate jälgida konfiguratsiooni edenemist üksikasjades.
8. Kui konfiguratsioon on lõpule viidud, valige **link Power Platform keskkonnale,** et sünkroonida saadaolevad andmeüksused.
9. Kui olek näitab, et keskkonnad on edukalt lingitud, Power Platform minge üle halduskeskusesse ja valige sobivad andmeüksused.
10. Valige vasakul paanil **Dynamics 365 rakenduste ressursid \>**.
11. Veenduge, et topeltkirjutusega inimressursside rakenduse olek on **lubatud**.
12. Valige topeltkirjutuse inimressursside rakendus ja seejärel valige käsk **Installi**.
13. Valige topeltkirjutuse **rakendusepaanil Dynamics 365 Human Resources** sobiv keskkond, kus pakett installida.
14. Valige märkeruut teenusetingimustega nõustumiseks ja seejärel valige käsk **Installi**.
15. Dynamics 365 rakenduse keskkonnas installitakse **olekut** installi ajal. See uuendatakse installi lõpuleviidud **versiooniks** Installitud.

##### <a name="review-and-apply-a-dual-write-solution"></a>Vaadake üle ja rakendage topeltkirjutuse lahendus

1. Minge uues finants- ja toimingute keskkonnas andmehalduse topeltkirjutusse **\>**.
2. Valige **rakenda lahendus**.
3. Valige paanil Dynamicsi installitud lahendused, topeltkirjutuse **rakenduste põhiüksuse vastekaardid** ja **vastekaardid**.**Dynamics 365 Human Resources** Seejärel valige **rakenda.** Teade kinnitab lahenduse rakendamist. Pärast lahenduse edukat rakendamist kuvatakse kõik saadaolevad tabeli vastekaardid.
4. Vaadake saadaolevad tabeli vastekaardid üle, et valida ja käivitada integratsioon topeltkirjutuse abil.
5. Topeltkirjutuse integratsiooni käivitamisel tabelikaartide esmakordsel käivitamisel valige märkeruut **Algne** sünkroonimine. Kui inimressursside lähtekeskkonnast on olemas integratsioon, **ei** pea te tabelikaartide integreerimise käivitamisel valima märkeruutu Algne sünkroonimine.

#### <a name="recommended-practices"></a>Soovitatavad tavad

Selles jaotises antakse soovitused eraldi infrastruktuurist finantside ja toimingute infrastruktuuride kaudu migreerimiseks.

- Soovitame tungivalt teil töötada partneriga Microsoft Dynamics, et saada abi inimressursside keskkonna migratsiooniga.
- Plaanige sobiv aeg täiskasutajate aktsepteerimise testimiseks (UAT) sisendkausta ülekantud keskkonnas.
- Saate plaanida ja dokumenteerida üksikasjalikud sammud ülekandmiskeskkonda integratsioonide migreerimiseks.
- Looge üksikasjalik kontroll-loend, et liigendada oma migratsiooni üleminekuprotsess.
- Planeerige ettevõttele migreerimise ajal sobiv hulk töötunde.
- Soovitame tungivalt, et FastTracki-kvalifitseeritud kliendid töötaks koos oma FastTracki lahenduse arhitektiga, et saada abi migratsiooniprotsessi eest.
- Soovitame tungivalt enne esimese migreerimist uuendada oma mälukasti keskkonda eraldi infrastruktuuris. See värskendus peaks hõlmama teie keskkonda Dataverse, mis on ühendatud boksikeskkonnaga, mida plaanite ülekandda.
- Soovitame tungivalt kasutada teenusekontot, kui juurutate, kannate üle ja loote oma elutsükli teenuste projekti.
- Plaanite uuendadaboxi keskkonda UAT-i valideerimiseks uusima üldise kättesaadavuse (GA) väljalaskes. Lisateavet vt [kaalutlustest](hr-infrastructure-merge.md#considerations).
