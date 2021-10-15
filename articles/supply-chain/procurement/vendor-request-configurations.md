---
title: Hankija nõude konfiguratsioonid
description: See teema kirjeldab välju, mis tuleb uue hankija taotluse puhul täita.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1d34a9974da41b7abb40bb2cf046a15432c249eb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570293"
---
# <a name="vendor-request-configurations"></a>Hankija nõude konfiguratsioonid
[!include [banner](../includes/banner.md)]

Hankija taotluse lõpetamiseks peab hankija kontaktisik läbima potentsiaalse hankija registreerimisviisardi.

Vormil **Hankija taotluse konfiguratsioonid** saate luua profiile, milles on määratud nõutud ja nähtavad väljad potentsiaalse hankija registreerimisviisardil.

Hankija registreerimisviisardi alguses küsitakse potentsiaalse hankija kasutajalt, millises riigis/regioonis hankija tegutseb. See teave määrab rakendatava konfiguratsiooni. Kui riigi/regiooni konfiguratsiooni pole määratud, kasutatakse vaikekonfiguratsiooni.

### <a name="set-up-a-vendor-request-configuration"></a>Hankija taotluse konfiguratsiooni seadistamine

Vaikimisi on hankija konfiguratsioon saadaval vormil Hankija taotluse konfiguratsioonid.

Vaikekonfiguratsiooni puhul ei saa riiki/regiooni valida, seega ei saa jaotises **Riigid/regioonid** muudatusi teha.

1. Klõpsake valikuid **Hanked** > **Seadistamine** > **Hankijad** ja seejärel klõpsake valikut **Hankija taotluse konfiguratsioonid**.
2. Loetletud üksustele oleku määramiseks klõpsake vahekaari **Väljad**.
3. Peidetud (pole nähtav)
4. Kuvatud (nähtav, kuid pole kohustuslik)
5. Nõutav (nähtav ja kohustuslik)
6. Määramaks, kas teksti kuvatakse viisardis ja kas potentsiaalse hankija kasutaja peab enne viisardis järgmise sammu juurde liikumist selle kinnitama, klõpsake vahekaarti **Sisu**. Kinnitamist küsitakse kõigi nõuete ja tingimuste puhul, millega kasutaja peab enne jätkamist nõustuma.

Võite sisestada ka kinnitusteate, mis kuvatakse, kui viisard on läbitud, samuti saate lisada ühe või mitu küsimustikku.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Hankija konfiguratsiooni loomine konkreetse riigi/regiooni jaoks
1.  Klõpsake valikuid **Hanked** > **Seadistamine** > **Hankijad** ja seejärel klõpsake valikut **Hankija taotluse konfiguratsioonid**.
2.  Uue konfiguratsiooni loomiseks klõpsake valikut **Uus** ja sisestage konfiguratsiooni nimi.
3.  Klõpsake nuppu **Salvesta**.
4.  Riigi/regiooni puhul kasutatava konfiguratsiooni valimiseks avage vahekaart **Riik/regioon**.
5.  Konfiguratsiooni lõpetamiseks järgige vaikekonfiguratsiooni juhiseid.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]