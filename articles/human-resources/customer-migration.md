---
title: Inimressursside kliendi siirde KKK
description: See artikkel vastab korduma kippuvatele küsimustele Microsofti migreerimise kohta Dynamics 365 Human Resources finantside ja toimingute ühendatud infrastruktuuri.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151095"
---
# <a name="human-resources-customer-migration"></a>Inimressursside kliendi migratsioon

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Kuidas peaksid Dynamics 365 Human Resources kliendid plaanima liikuda finantside ja toimingute infrastruktuuri?

Mõjutatud on kaks Microsofti Dynamics 365 Human Resources kliendikategooriat ja need peavad tegema muudatused, et veenduda, kas need on viimases finantside ja toimingute infrastruktuuris.

- Kliendid, kes kasutavad Dynamics 365 Human Resources rakendust Dynamics 365 ja kellel ei ole muid toimingute rakendusi
- Kliendid, kes kasutavad nii Dynamics 365 Human Resources rakendust Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce või Dynamics 365 Project Operations

Sõltumata kategooriast, kuhu nad kuuluvad, peavad kliendid teisaldama andmed äsja loodud keskkonda finantside ja toimingute infrastruktuuris ning kinnitama, et ühendamine on edukalt lõpetatud.

Rakendusel on oma Dynamics 365 Human Resources finants- ja toimingute keskkond, mis on teistest toimingute rakendustest eraldi. Sel viisil saavad kliendid laiendatavusvalikuid kasutada ilma praegusi andmeid ühendamata. Microsoft pakub tööriistade ja sisendkausta keskkondt, mida kliendid saavad kasutada andmesiirde testimiseks ja kinnitamiseks, enne kui nad tootmiskeskkonda teisaldavad. Tööriista kasutamine võimaldab lähedalasuva automatiseeritud protsessi ja on saadaval vahemikus augustist novembrini 2022.

Kliendid, kes kasutavad teisi rakendusi finantside ja toimingute infrastruktuuris, on võimalik ühendada oma Inimressursside andmed olemasoleva keskkonnaga. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Millal viiakse kliendid üle finantside ja toimingute infrastruktuuri?

Iga ettevõtte üleminekud sõltuvad ettevõtte praegusest konfiguratsioonist ja valmisolekust liikuda finantside ja toimingute infrastruktuuri. Soovitame, et kliendid töötaks koos oma Microsofti partneriga, et määratleda parim edasisuunas tee.

- Organisatsioonid, mis **kasutavad** Dynamics 365 Finance Dynamics 365 Human Resources moodulit Inimressursid, saavad lubada uusi võimalusi tavalise versiooni uuendamise protsessi osana. Uute funktsioonide muutumine üldiselt kättesaadavaks alates 2022. jaanuarist.
- Seda kasutavad Dynamics 365 Human Resources organisatsioonid pääsevad juurde tööriistadele, mida nad saavad kasutada infrastruktuuride ühendamise lõpetamiseks. Microsoft töötab klientidega siirde ajal, et vältida teenuse katkestust. Klientidel on üleminekuks 12–18 kuud, alustades ajast, mil migreerimise tööriist muutub kättesaadavaks.
- Organisatsioonid, mis kasutavad Dynamics 365 Human Resources nii moodulit **Inimressursid** kui ka saavad teisaldada oma autonoomse inimressursside infrastruktuuri finantside ja toimingute infrastruktuuri. Teise võimalusena saab kasutada ühendamise tööriista keskkonna toomiseks ühte keskkonda. Kahe keskkonna ühendamiseks pole mingit nõuet ega ajavahemikku.

Uuendatud teabe saamiseks kontrollige regulaarselt [väljalaskeplaane](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Kas kliendid vajavad siiski kohandatud integratsiooni inimressursside Dynamics 365 Human Resources mooduli vahel?

- Kliendid, kellel on nii Dynamics 365 Human Resources kui teised finantside ja toimingute infrastruktuuri keskkonnad, mis on praegu integreeritud, peavad pärast ühendamist jätkama kahe keskkonna integreerimist.
- Kliendid, kes valivad Dynamics 365 Human Resources oma keskkonna eraldi olemasolevatest finantside ja toimingute rakenduse keskkonnast, peavad jätkama keskkondade integreerimist, et teha andmed mõlemas keskkonnas kättesaadavaks.
- Kliendid saavad andmete integreerijat kasutada andmete kopeerimiseks kahe keskkonna vahel. Kliendid, kes kooste andmed pärast siirdet ühte keskkonda, ei pea enam andmeid integreerima, kuna kõik andmed on ühte andmebaasi.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Kas kliendi ISV lahendused migreeritakse automaatselt?

Iga sõltumatu tarkvaratootja (ISV) lahenduse üleviimise kogemus varieerub sõltuvalt lahenduse integreerimismeetodist. Microsoft teeb isV-ga koostööd, et pakkuda ühtlane üleminekut finantside ja toimingute infrastruktuurile. Paljud ISV lahendused on üleseetud Dataverse võimaluste abil Microsoft Power Platform. Need lahendused sõltuvad keskkonna Dataverse ja keskkonna Dynamics 365 Human Resources vahelisest integratsioonist Dataverse. Integratsioon Dataverse on infrastruktuuri ühendamise osana mittetauniv. Finantside ja toimingute infrastruktuuris plaanitakse uued topeltkirjutuse kaardid integratsiooni funktsiooni välja vahetama Dataverse.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Kuidas mõjutab see andmete integreerija, mis teisaldab andmeid Dynamics 365 Human Resources dynamics 365 rakenduste vahel?

Kui kliendid on teisaldanud finantside ja toimingute infrastruktuuri, tuleb neil jätkata andmete integreerimist kahe keskkonna vahel. Kliendid saavad andmete migratsiooni ülesannete sooritamiseks jätkuvalt kasutada andmeintegraatorit. Kliendid, kes plaanivad hoida Dynamics 365 Human Resources oma keskkonda eraldi oma olemasolevatest finantside ja toimingute rakenduste keskkonnast, peavad andmete integreerimist kahe keskkonna vahel jätkama. Klientide puhul, kes ühendavad need kaks keskkonda ühte keskkonda, ei nõuta enam integratsiooni kahe keskkonna vahel.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Kuidas andmeid teisaldatakse finantside Dynamics 365 Human Resources ja toimingute infrastruktuuris ning pärast Dataverse migreerimist?

Praegune integratsioon Dataverse finantside Dynamics 365 Human Resources ja Dataverse toimingute infrastruktuuri osana ja see on taunitud. Plaanitakse kasutusele võtta topeltkirjutuse kaardid, et vastendada finantside ja toimingute üksused tabelitega Dataverse. Kliendid peavad otsustama, millised topeltkirjutuse kaardid on nende rakendamiseks vajalikud. Me soovitame kasutada integratsioonide ja ISV lahenduste jaoks virtuaaltabeleid, välja arvatud juhul, Dataverse kui äriloogika käivitamiseks on vaja andmeid dubleerida.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Kuidas mõjutab migratsioon laiendusi Dataverse Dynamics 365 Human Resources?

Kliendid peavad enne tootmiskeskkonna üle siirdamist siirdamaboxi keskkonda. Kui kliendid oma sisendkausta keskkonda üle kannavad, tuleb Dataverse neil luua keskkonnast koopia, et ühenduda uute finantside ja ülekantud operatsioonide keskkonnaga. Soovitame kliendil kopeerida nii andmed kui ka keskkonnalahendused, et need sobiksid kliendi praeguse tootmiskeskkonnaga.

Kui kliendid on valmis oma tootmiskeskkonda üle kandma Dynamics 365 Human Resources, siirdab Microsoft andmebaasi ja Azure Blobi lao automaatselt üle. Migreeritud andmebaas ja talletus suunavad uue keskkonna finantside ja toimingute infrastruktuuris samale tootmiskeskkonnale Dataverse. Enne kui andmeid saab Dataverse edasi kopeerida, peavad kliendid lubama mis tahes topeltkirjutuse kaardid, mis on vajalikud nende integratsioonide, laienduste ja ISV lahenduste jaoks, mis on üles ehitatud Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Kas Microsoft Power Platform automaatselt loodud komponendid töötavad Dynamics 365 Human Resources pärast infrastruktuuri siirde lõpetamist?

Rakenduses loodud rakendused Power Apps, vood, mis on loodud Power Automate ja muud kohandused Microsoft Power Platform, nagu laiendid Dataverse. Kliendi tootmiskeskkondade migreerimise ajal puudub mõju Dataverse keskkonnale, k.a laiendid. Rakendused, vood ja muud Power Microsoft Platformi kohandamised peaksid tööd jätkama ilma lisakonfiguratsiooni nõudmata.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Mida teha virtuaaltabeli Dataverse üksustega migreerimise Dynamics 365 Human Resources ajal?

Kui kliendid kannavad Dynamics 365 Human Resources oma keskkonda üle finantside ja toimingute infrastruktuuri, jääb Dataverse keskkond alles ühendatud keskkonnaga, mis on hetkel ühendatud Dynamics 365 Human Resources. Keskkonnas Dataverse loodud virtuaaltabelid jätkavad tööd ilma lisakonfiguratsiooni nõudeta. Võimalik, et virtuaalsed tabelid tuleb uuesti luua keskkonnas Dataverse, mis on ühendatud kliendi olemasoleva finants- ja toimingutekeskkonnaga.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Kuidas hakkab integreerimine, mis kasutab kandidaadi jälgimissüsteemi (ATS) API-d, palga API-d, Dataverse Dynamics 365 Human Resources Dataverse virtuaaltabeleid või muid Web API töö üksusi pärast infrastruktuuri ühendamise lõpetamist?

Kui kliendid kannavad Dynamics 365 Human Resources oma keskkonda üle finantside ja toimingute infrastruktuuri, jääb Dataverse keskkond alles ühendatud keskkonnaga, mis on hetkel ühendatud Dynamics 365 Human Resources. Kõik veebi API suhtes välja töötatud Dataverse integratsioonid jätkavad tööd pärast migreerimise lõpetamist.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Meie organisatsioon on konfigureerinud kohandatud turvalisuse töös Dynamics 365 Human Resources. Kas see rakendatakse endiselt pärast infrastruktuuri migreerimise lõpetamist?

Jah, andmesiirdesse kaasatakse kohandatud turvakonfiguratsioonid.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Kas töövood migreeritakse Dynamics 365 Human Resources automaatselt?

Jah, töövoo konfiguratsioonid, töövoo ajalugu ja praegused protsessi töövood migreeritakse ühendatud infrastruktuuri.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Kas salvestatud vaated Dynamics 365 Human Resources migreeritakse automaatselt?

Jah, salvestatud vaated migreeritakse ühendatud infrastruktuuri.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Kas automaatselt lubatud funktsioonid on Dynamics 365 Human Resources pärast infrastruktuuri ühendamist saadaval?

- Klientide puhul, kes kasutavad inimressursside **moodulit**, hallatakse funktsioonihalduse Dynamics 365 Human Resources kaudu ainult saadaolevaid funktsioone. Tavaliselt ei lubata neid funktsioone vaikimisi. Kõik vaikimisi lubatud funktsioonid dokumenteeritakse.
- Kliente, kes Dynamics 365 Human Resources kasutavad, on funktsioonid infrastruktuuris saadaval. Dokumenteeritakse kõik funktsioonid, mis pole saadaval. Kõik praeguses keskkonnas lubatud funktsioonihalduse Dynamics 365 Human Resources võtmed lubatakse ühendatud infrastruktuuris. Lisateavet vt [Funktsioonihalduse ülevaatest](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Mis juhtub BYOD andmebaasidega migreerimise ajal?

Impordi ja ekspordi konfiguratsioonid oma andmebaasi (BYOD) toomiseks migreeritakse finantside ja toimingute infrastruktuuri.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Kas kliendikeskkonna migreerimisel mõjub Azure'i regioon?

Keskkond Dynamics 365 Human Resources jääb migreerimiseks samasse Azure'i regiooni. Kui on nõue viia keskkond teise Azure'i piirkonda, peavad kliendid järgima standardtoiminguid, et migreerida uude piirkonda pärast migreerimise lõpetamist.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Mis juhtub Azure'i andmetega migreerimise ajal?

Mis tahes ekspordil, mis on praegu konfigureeritud Azure DataAmeti jaoks finantside ja toimingute rakendustes, säilitatakse pärast migreerimist sama konfiguratsioon.

> [!NOTE]
> Topeltkirjutuse kaardid peavad olema lubatud, et jätkata andmete kirjutamist inimressursside keskkonnast sellesse Dataverse.

Kliendid, kes soovivad eksportida Inimressursside andmeid andmetesse, võivad selle funktsiooni lubada pärast finantside ja toimingute infrastruktuuri siirdamist. Lisateavet vt jaotisest Data [blos – Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

Kliendid saavad linkida mitu finants- ja operatsioonide keskkonda sama andmega. Iga keskkond osutab siiski erinevale kaustale ja konteinerile. Kliendid, kes plaanivad hiljem keskkondi ühendada, peaksid oma lähenemist hoolikalt planeerima.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Milline migratsioon on vajalik, kui klient kasutab praegu inimressursside moodulit?

Kliendid, kes kasutavad **Inimressursside moodulit** saavad uued Dynamics 365 Human Resources funktsioonifunktsioonid rakendada oma keskkonda standardse ühe versiooni uuendamise protsessi kaudu. Kliendid võivad eeldada uusi funktsioone oma keskkonnas, nagu see muutub kättesaadavaks igas värskenduses. Kliendid saavad funktsioonide lubamiseks funktsioonihaldust kasutada. Kliendid peaksid plaanima need uued funktsioonid kinnitada, kasutades protsesse, mis neil juba on olemas, ja neid kasutatakse oma keskkonnas muude uuenduste kinnitamiseks.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Mida teha kohandatud integratsioonidega välissüsteemidega?

Kliendid peavad oma integratsioonid ülekandma finants- ja operatsioonide keskkonda. Kuna selle keskkonna lõpp-punkt on erinev, võivad kliendid integratsioonid uuendada või muuta nii, et nad osutavad uuele keskkonnale. See ülesanne on peamiselt käsitsi protsess ja vajalikud muudatused sõltuvad integratsiooni arhitektuurist. Kliendid peaksid tegema koostööd oma Microsofti partneriga, et määrata parim viis liikuv integratsioonide jaoks.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Mis toimub () Microsoft Power Platform laienditega Dataverse, kui kliendid ühendavad keskkonna Dynamics 365 Human Resources olemasoleva finants- ja operatsioonide keskkonnaga?

Kui kliendid otsustavad Dynamics 365 Human Resources Dataverse ühendada keskkonna ja olemasoleva finants- ja toimingute keskkonna üksikeksemplariks pärast siirdeid, Dataverse tuleb nende keskkonnad ühendada ühendamisprotsessi osana. See ülesanne nõuab, et kõik rakendusi, mis on loodud kasutades Power Apps ja mis tahes muid kohandusi, tuleks uues keskkonnas uuesti juurutada.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Mida teha dokumentidega migreerimise ajal?

Kui kliendid kannavad Dynamics 365 Human Resources oma keskkonda üle finantside ja toimingute infrastruktuuri, jäävad dokumendid olemasolevasse dokumendisalvestusse ja vastendatakse automaatselt uude keskkonda finantside ja toimingute infrastruktuuris.

Tulevases väljaandes antakse uued andmeüksused. Pärast seda muudatust saavad kliendid, kes Dynamics 365 Human Resources valivad oma keskkonna ühendamise olemasoleva finants- ja operatsioonide keskkonnaga, eksportida dokumente ja teisaldada need olemasolevasse keskkonda.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Mis toimub pärast migreerimist nende pakett-töödega, mis on konfigureeritud Dynamics 365 Human Resources?

Pakett-tööd tuleb finants- ja toimingute keskkonnas ümber konfigureerida. Kliendid peavad hindama iga pakett-tööd ja võrdlema seda praeguse pakett-tööde loendiga finants- ja toimingute keskkonnas. Kliendid peaksid kahe pakett-töö komplekti ühendamisel analüüsima ka üldist partiigraafikut, et määrata, kas partii graafikusse, prioriteetidesse või partiigruppidesse tuleb teha muudatusi.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Kuidas mõjutab migratsioon LCS-projekti Dynamics 365 Human Resources?

Kliendid peavad looma Microsoft Dynamics uue elutsükli teenuse (LCS) **projekti** ja nad peavad projektitüübina valima finantside ja toimingute rakendused tootena ja rakendusena. Lisaks on alamprojekti tüübi uus väli saadaval LCS-projekti loomisel. Kliendid peavad valima suvandi migreerimiseks, Dynamics 365 Human Resources et kanda olemasolev Inimressursside LCS-projekt üle finantside ja toimingute infrastruktuuri.

Finantside ja toimingute LCS-projektide funktsioonid erinevad inimressursside LCS-i projektide funktsioonidest.

Reaalajas peavad uued kliendid lõpule täitma järgmised ülesanded:

- Lõpeta projekti sisseuhtestamine.
- Viige metodoloogia lõpule.
- Saate sisestada kordustellimuse väljastaja.
- Lõpetage otse-reaalajas valmisoleku protsess.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Kuidas äriprotsessi mudeldajat üle siirdatakse?

Kliendid peavad eksportima oma äriprotsesside modelleerimisteegi Inimressursside LCS-projektist ja importima selle finantside ja toimingute LCS-projekti. Lisaks peavad kliendid uuendama rakenduse Spikri sätteid nii, et nad osutavad uuele LCS-projektile.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Kuidas mõjutab migreerimine teenuse värskendusprotsessi?

Pärast migreerimist on klientidel rakenduse elutsükli halduse (KORRALDUS) ja teenuse värskenduste osas palju paindlikum. Teenuse värskendusi ei rakendata enam automaatselt inimressursside keskkondades. Selle asemel järgib teenus Ühe versiooni teenuse värskendusprotsesse ja funktsioone ning LCS-i kaudu värskenduste konfigureerimisvalikud lubatakse.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Kas kliendid on infrastruktuuri ühendamisel FastTracki abi saamiseks kõlblikud?

Microsoft määratleb endiselt, millised tööriistad ja ressursid on FastTracki abil ühendamisel saadaval.

## <a name="licensing-impact"></a>Litsentsimise mõju

Lisateavet litsentsimise mõjutamise kohta vaadake infrastruktuuri ühendamise [Dynamics 365 Human Resources KKK-st](hr-infrastructure-merge-faq.md#licensing-impact).
