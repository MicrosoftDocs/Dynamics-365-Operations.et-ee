---
title: Ennetavad kvaliteediuuendused
description: See artikkel annab teavet kvaliteediuuenduste ennetava tarne kohta.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338132"
---
# <a name="proactive-quality-updates"></a>Ennetavad kvaliteediuuendused

[!include[banner](../includes/banner.md)]

Viimase mitme aasta jooksul on Microsoft teinud pidevat edenemist selle osas, mida me nimetame üheks [versiooniks](../../dev-itpro/lifecycle-services/oneversion-overview.md). Ühe versiooni eelne on lihtne: mida lähemal on võimalik saada kõigi klientideni sama tarkvaraversiooni puhul, seda kõrgem on kvaliteet, mida suudame tarnida. Probleemid leiab ja lahendatakse üks kord ning need lahendused võetakse rohkematest klientidest kiiremini.

Selle eelduse kinnitavad tulemused: väiksem juhtumite arv kõigis meie toodetes. Kui kliendid ei ole samas versioonis, oleme järjepidev, et neid mõjutavad probleemid, mille jaoks lahendus on juba saadaval. Oleme juba teinud suurt edu Dynamics 365 Finance’i, Dynamics 365 Dynamics 365 Project Operations Dynamics 365 Commerce tarneahelaga ja tänu viimastele tehnilistele ettemaksetele on nüüd võimalik teha järgmine samm. Järgmine teave annab välja selle, mida me kavatseme teha, mida oleme juba etapi kehtestab ning kuidas ja millal me uusi võimalusi katkestuseta tutvustame.

## <a name="focus-on-quality-updates"></a>Fookus kvaliteediuuendustele

Pakume praegu 7 [teenuseuuendust](public-preview-releases.md) aastas. Näiteks versioon 10.0.29 on teenuse värskendus. Kuni viimaseni uuendati aasta kohta kaheksat uuendust. Kuid me kukutasime ühe värskenduse vastuseks kliendi tagasisidele, mis soovis vältida muudatusi kalendriaasta lõpus.

Teenuse uuenduste sagedust ei muuda me. Selle asemel keskendub meie järgmine samm edasi ühe versiooni reisil *kvaliteediuuendustele*. Kvaliteediuuendused on kiirparanduste kumulatiivsed järgud. Need ei sisalda uusi funktsioone. Mis tahes aja jooksul on kogu meie klientide ühendus erinevusi kolme või nelja kõige viimase teenuse uuenduse vahel. Iga teenusevärskenduse puhul saab siiski kasutada grupi sees tosinat erinevat kvaliteedivärskenduse versiooni, sõltuvalt juurutatud inimeste kuupäevadest. Järgmise sammuna levitame ennetavalt kvaliteediuuendusi. Me juba kasutame seda mudelit meie - Dataverse põhiste rakenduste jaoks ning oleme pidanud nägema eeldatavaid kvaliteedi parandamise ja vähenenud tugijuhtumite tulemusi.

Defektide vähenemine võib muidugi vähendada või täielikult eemaldada kvaliteediuuenduste vajaduse. Meil on lennus mitu algatused kvaliteediuuendust nõudva defekti vähendamiseks. Isegi siis, kui kvaliteedi uuendamisel vähendatakse töökoormust, parandab järjepidevus kliendibaasi kaudu tugitavust, tagab klientide parendusi kiiremini ja vähendab klientide sagedust lahenduste juba olemas olemise probleemi korral.

## <a name="making-proactive-distribution-possible"></a>Ennetava jaotuse võimalikuks tegemine

Mitmed ettemaksed on juba juurutatud, mis võimaldavad kvaliteediuuenduste ennetavat tarnimist:

- **Nullväärtusega downtime-uuendamine** – sagedaste keskkondade tõukamiseks on oluline vähendada mõju keskkonna saadavusele, et säilitada Dynamics 365 teenustaseme lepingud (SLAs). Algselt juurutati nullväärtusega ajaline uuendamine, et aidata parandada kuu operatsioonisüsteemi paikamist klastri ülemineku abil värskendatud pildi aktiveerimiseks minimaalse katkestusega. Uuenduste rakendamise mehhanism on täiustatud nii, et see oleks veel vähem katkestav ning kataks nii operatsioonisüsteemi paikamise kui ka kvaliteediuuenduse juurutamise.

    Interaktiivsete kasutajate puhul võib aktiivne seanss katkeda ja uuesti käivitatakse uuesti uuendatud keskkond. Prioriteedipõhise partiiplaneerimise [juurutamisel](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), mis on nüüd saadaval liitumise alusel, taastab pakkplaneerimine ja töötlemine ning jätkab tööd kohe pärast uuendamist. Prioriteetne pakkplaneerimine toimub klientide jaoks enne, kui nad hakkavad osalema oma tootmiskeskkondades kvaliteediuuenduste ennetavas jaotuses.

- **tumetunnid** – tume tunnid on määratud igale Azure’i piirkonnale ja lähedalasuvad null ajaperioodi värskendused tekivad tumetunnise perioodi jooksul.

## <a name="the-proactive-update-process"></a>Ennetav uuendusprotsess

Ennetava kvaliteedivärskenduste juurutamine järgib seifijuurutusprotsessi (SDP). SDP spetsiifilised reeglid muutuvad, kuid kvaliteediuuendused juurutatakse algselt kaustakeskkonda. Protsess algab keskkondadega, mis nõustuvad varajase juurutamisega. Kui edukalt juurutatud bokside protsent suureneb, algab juurutamine tootmiskeskkondades. Taas kord algab protsess keskkondadega, mis valivad varajase juurutamise. Kuulamissüsteem jälgib süsteemi telemeetriat ja livesite’i juhtumeid ning peatab konkreetse versiooni väljapööramise, kui tuvastati regresssioon. Kliendid saavad siiski enne enne enne juurutamist kvaliteedivärskendusi tõmbada, kui nad seda soovivad.

Praegused väljalaskehalduse andmed näitavad, et kvaliteediuuendustele tutvustatakse vähem kui 3 protsenti regressioone. Suurenenud fookuse eemaldamisel regressiooni ja täiustatud SDP-ni on regressioone potentsiaalne mõju potentsiaalselt väiksem kui kvaliteedikasumid, mis on klientide jaoks paranduste kiiremaks juurutamise teel saavutatav.

## <a name="process-changes"></a>Protsessi muudatused

Protsessimuudatuste kogum rakendatakse enne enne kvaliteedivärskenduse juurutamist.

- **Skeem**: tööriistamine tagab, et kvaliteedivärskenduse järgud sisaldavad ainult skeemi muudatusi, mida saab rakendada, kui teenus on võrgus. See lähenemine aitab säilitada võimalust rakendada uuendust nullväärtusega downtime’iga.
- **Aktiivsete muudatuste** muutumine on juba täiendav protsessisamm, et kinnitada muudatused kvaliteedivärskendusse kaasamise jaoks. Regressioone võimalike vähendamiseks suurendatakse lisasammide edasist haldust. Kvaliteediuuenduste puhul pole katkestatud muudatused lubatud ja suurenenud muudatus aitab tagada, et vastame sellele sihile.
- **Nähtavus** – me saadame teatised meili ja elutsükli teenuste (LCS) kaudu eesseisva ennetava kvaliteediuuenduse jaoks. Lisaks on tugimeeskonnad ja juhtumi vihjed nähtavusega seal, kus kvaliteediuuendused on ennetavalt juurutatud.
- **Versiooni varuversioon** – lennuteed kasutatakse kõikide muutuste grupeerimiseks proaktiivses kvaliteedivärskenduses. Kui tagasipöördumine on vajalik pärast ennetavat juurutamist, saab seda teha lennusüsteemi kaudu.
- **Windowsi sünkroonimise määramine** – vähem kui 20%-l klientidest on täna mitu ruutu ja ühe boksi juurutamiseks on versiooni vastendamise tootmisse juurutatud, et aidata teil tõrkeotsingut. Tulevikus tutvustame klientidele võimalust määrata sisendkausta keskkond, mis ei peaks saama ennetavat kvaliteedivärskenduse juurutamist koos teiste kaustadega, kuid see peaks selle saama hiljem koos tootmiskeskkonnaga. Pange tähele, et kui klient kasutab märkeruutu uuema versiooni testimiseks kui nende tootmises, saab see kastist uuema versiooni kvaliteediuuendused.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Millal käivitatakse ennetavad kvaliteediuuendused?

Ennetava kvaliteediuuenduste jaotus sisendkausta keskkondades peaks eeldatavasti algama septembri lõpus või septembril 2022 Azure’i avaliku pilve klientidele. Proovikeskkonnad hakkavad saama ka sel ajal ennetavat uuendamist. Septembris saadetakse kliendile teatis, mis teavitab neid eeldatavast keskkonnagraafikust. Ennetava värskendatud jaotusprotsessi erandid on lubatud ainult FDA-ga reguleeritud klientide puhul. Töötame endiselt selles, kuidas hallatakse reguleeritud keskkondi ja ande- ja valitsuse pilve kliente.

Järgmise kuue kuu jooksul suurendame järk-järgult märkeruutukeskkondade protsenti, mis saavad ennetavad uuendused, kuni kõik määratud keskkonnad on kaasatud ja edenemine tootmiskeskkondade uuendamisel. Kogu perioodi jooksul jälgime, kindlustamaks, et juurutusprotsess on tõrgeteta ja et me saada kätte meie mitteladustavate lastide sihtmärgi.

Kuna kliendid saavad regulaarselt väiksemaid töökoormusi, eeldame, et praegused täitjad muutuvad lihtsamaks. Korrigeerime juurutamise uuendamise sagedust vastavalt võimele protsessi käivitada katkestuseta. See protsess töötab juba tõhusalt meie platvormi ja Dataverse rakenduste jaoks ning pakub teenuse kvaliteedi eeldatavat parendust. Soovitame teha sama sammu edasi finants- ja operatsioonide rakenduste puhul.
