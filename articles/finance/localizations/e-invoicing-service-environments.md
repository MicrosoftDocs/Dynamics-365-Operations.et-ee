---
title: Teenusekeskkonnad
description: See artikkel annab teavet elektroonilise arveldamise teenusekeskkonna kohta ja selgitab nende häälestamist.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8c743c5b2fbc7dcc3ae04fa4d7ca0e65de6c2507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901243"
---
# <a name="service-environments"></a>Teenusekeskkonnad

[!include [banner](../includes/banner.md)]

Teenusekeskkonnad on loogilised sektsioonid, mis luuakse globaliseerimisfunktsiooni toetamiseks ja vastavaid dokumente, mida töödeldakse elektroonilise arveldamise teenuses. Turvasaladused ja digitaalsed tunnistused ning pääsuõigused (juhtimine) peavad olema konfigureeritud teenusekeskkonna tasemel.

Saate luua nii palju teenuse keskkondi, kui vaja. Kõik teie poolt luuavad teenusekeskkonnad on üksteisest sõltumatud. Soovitatav on luua vähemalt kaks teenuskeskkonda:

- Üks keskkond peamisteks arendus- ja kinnitamiseesmärkideks. See keskkond on tavaliselt kasutaja nõustumise testimise (UAT) keskkond.
- Üks keskkond tootmise eesmärgil. Tavaliselt on see keskkond tootmiskeskkond.

Seda tüüpi sektsioonimine aitab tagada, et e-arve protsessid kinnitatakse ja kohandatakse kaustas enne, kui nad tootmisse lähevad.

Teenusekeskkonnad tuleb luua ja hooldada regulatiivse konfiguratsiooni teenuses (RCS). Seejärel, kui nad on valmis, tuleb need avaldada Elektroonilise arveldamise teenuses. Avaldamisprotsess saadab teenusekeskkonna parameetrid RCS-i eksemplarist elektroonilise arveldamise teenusesse.

Kui te ei lõpeta avaldamisprotsessi pärast uue teenusekeskkonna loomise või olemasoleva teenusekeskkonna korrigeerimist (Microsoft Azure nt kasutajate lisamise või eemaldamise või vaultvõtme saladuste lisamisega), siis need muudatused ei jõustub. Dynamics 365 Finance või Dynamics 365 Supply Chain Management.

## <a name="service-environment-statuses"></a>Teenusekeskkonna olekud

Teenuse keskkondi saab hallata läbi nende oleku. Keskkonna olekut saate vaadata lehel **Teenuse keskkonnad**. Saadaval on järgmised olekud:

- **Pole avaldatud** – keskkond on loodud, kuid seda pole veel avaldatud.
- **Avaldatud** – keskkond on avaldatud elektroonilise arveldamise teenusesse.
- **Muudetud** – avaldatud keskkonna atribuute on muudetud, kuid muudatusi pole veel avaldatud.

## <a name="users"></a>Kasutajad

Iga teenusekeskkond peab loetlema kasutajad, kes saavad finants- või tarneahela halduses luua ühenduse elektroonilise arveldamisega.

## <a name="applications"></a>Avaldused

Mõne stsenaariumi korral võivad muud rakendused peale finantside või tarneahelate halduse ühenduda elektroonilise arvelduse teenusega, et esitada edasiseks töötlemiseks elektroonilisi dokumente, või hankida sellist teavet, nagu dokumendi esitamise olek. Nende stsenaariumide puhul tuleb avaldus määratleda avalduste loendis. Sel viisil on sel juurdepääs elektroonilise arvelduse teenusele. Rakendus peab olema registreeritud ka rakendusena Azure Active Directory (Azure AD) ja objekti ID-d tuleb kasutada selle tuvastamiseks. 

Kuna Microsoft nõuab kõrget turvakontrolli rakenduste üle, mis võivad ühenduda elektroonilise arveldamise teenusega, <DGXRegulatoryservicesengineering@service.microsoft.com> peate Ühendust Microsoftiga ja esitama oma rakendusele järgmised üksikasjad:

- Azure AD-i rentniku ID
- Microsoft Dynamics Elutsükli teenuste (LCS) keskkonna ID
- Rakenduse ID (kliendi ID)
- Objekti ID
- Rakenduse põhjendus ja kõrge taseme kirjeldus

Microsoft hindab taotlust ja registreerib rakenduse turvaregistris, et tagada selle võimalik käitamine elektroonilise arveldusega.

## <a name="number-sequences"></a>Numbriseeriad

Kui teie stsenaariumid nõuavad numbriseeriaid (näiteks failinimedes), saate kasutada numbriseeriaid, mis on määratud konkreetse keskkonna jaoks, kuid mida saab kasutada kas läbi kogu globaliseerimisfunktsiooni või konkreetse globaliseerimisfunktsiooni jaoks. Pärast numbriseeria määratlemist saate seda kasutada muutujates ja müügivõimaluste töötlemisel. Selle kasutamise jälgimiseks otsige numbriseeriate **lehel** parameetri Kasutuses **väärtust** **väärtusest** Praegune.

### <a name="working-with-number-sequences"></a>Numbriseeriatega töötamine
**Numbriseeriate** lehel: 

- Numbriseeria **loomiseks** valige väärtus Uus. Seejärel sisestage nimi ja kirjeldus. 
- Kui **numbriseeriat** enam ei kasutata, valige kustutamisjärjestus.
- Muudatuste avaldamiseks numbriseerias **ei** pea te tegevuspaanil valima käsku Avalda. Uuendamine toimub automaatselt.

## <a name="create-a-key-vault-reference"></a>Võtme hoidla viite loomine

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.
3. **Valige tegevuspaanil** Keskkonna häälestuslehelt **teenusekeskkonnad**.
4. Teenuse keskkondade **lehel**, valige tegevuspaanil võtme **hoidla parameetrid**.
5. **Võtme hoidla parameetrite lehel valige** võtme **hoidla** viite loomiseks uus.
6. **Sisestage väljale** Nimi võtme hoidla viite nimi.
7. Väljale **Kirjeldus** sisestage kirjeldus.
8. URI **võtmeväljal** kleepige võtme vault URI võtmehoidlast (`https://<your key vault>.vault.azure.net/`). Lisateavet vt Azure'i [võtme vault loomisest Azure'i portaalis](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Valige käsk **Salvesta**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Looge salvestuskonto salalubade jaoks saladus

1. Valige lehel **Võtme Hoidla parameetrid** võtme vaultviide, mille lõite eelmises protseduuris **,** ja seejärel valige jaotises Sertifikaadid suvand **Lisa**.
2. Väljal **Nimi** sisesta salvestuskonto saladuse nimi. See nimi peab vastama võtme vault-saladuse nimele, mis sisaldab salvestuse ühiskasutuses juurdepääsu allkirja (SAS) luba. Lisateavet vt Azure'i [ladustamiskonto loomine Azure'i portaalis](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. Väljalt **Tüüp** valige **Vali**.
5. Valige käsk **Salvesta**.
    
## <a name="create-a-service-environment"></a>Teenusekeskkonna loomine

1. **Teenusekeskkonna loomiseks** valige lehel **Teenuse** keskkonnad suvand Uus.
2. **Sisestage** väljale Nimi elektroonilise arvelduse keskkonna nimi.
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. Valige väljal **Salvestuskonto SAS-tõendi saladus** salvestuskonto juurdepääsu autentimiseks kasutatava serdi nimi.
5. Valige jaotises **Kasutajad** suvand **Lisa**, et lisada kasutaja, kellel on lubatud edastada elektroonilisi arveid keskkonna kaudu ja luua ühendus salvestuskontoga.
6. Sisestage väljale **Kasutaja ID** kasutaja pseudonüüm. 
7. Sisestage väljale **E-post** kasutaja e-posti aadress.
8. Valige käsk **Salvesta**.
9. Tegevuspaanil valige suvand **Avalda**, et avaldada keskkond elektroonilise arveldamise teenuses. Kontrollige, et välja **Olek väärtus** muudetakse väärtuseks **Avaldatud**.
