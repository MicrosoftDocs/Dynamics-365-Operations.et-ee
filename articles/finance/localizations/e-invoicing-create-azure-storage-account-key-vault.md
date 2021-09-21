---
title: Azure'i salvestusruumi konto ja võtmehoidla loomine
description: Selles teemas selgitatakse, kuidas luua Azure'i salvestusruumi kontot ja võtmehoidlat.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463838"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Azure'i salvestusruumi konto ja võtmehoidla loomine

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud sammude läbimist peate veenduma, et järgmised ülesanded oleksid lõpetatud.

- Võtmehoidla ressursi loomine Azure'is. Lisateavet leiate teemast [Teave Azure'i võtmehoidla kohta](/azure/key-vault/general/overview).
- Azure'i salvestusruumi konto loomine (bloobimälu). Lisateavet leiate jaotisest [Azure'i salvestusruumi konto haldamine](/azure/storage/blobs/).

## <a name="overview"></a>Ülevaade

Selles teemas läbite kaks peamist sammu.

- Azure'i salvestusruumi konto seadistamine salvestusruumi konto URI hankimiseks.
- Võtmehoidla seadistamine salvestusruumi konto URI talletamiseks.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Azure'i salvestusruumi konto seadistamine salvestusruumi konto URI hankimiseks

1. Avage salvestusruumi konto, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.
2. Avage **Andmehoidla** > **Konteinerid**, ja looge uus konteiner.
3. Sisestage konteineri nimi ja seadke välja **Avaliku juurdepääsu tase** väärtuseks **Privaatne(anonüümse juurdepääsuta)**.
4. Avage konteiner ja seejärel **Sätted** > **Juurdepääsupoliitika**.
5. Valige **Lisa poliitika**, et lisada talletamise juurdepääsupoliitika.
6. Seadistage väljad **Identifikaator** ja **Load** oma vajaduste järgi. Väljal **Load** peaksite valima kõik load.

    ![Bloobimälu loa andmine.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Sisestage algus- ja aegumiskuupäev. Aegumiskuupäev peab olema tulevikus.
8. Valige **OK** poliitika salvestamiseks ja seejärel salvestage muudatused konteineris.
9. Minge **Sätete** > **Jagatud juurdepääsutõendid** ja seadke välja väärtused. 
10. Sisestage algus- ja aegumiskuupäev. Aegumiskuupäev peab olema tulevikus.
11. Valige **Õiguste** väljal järgmised õigused: **Lugemine**, **Lisamine**, **Loomine**, **Kirjutamine**, **Kustutamine** ja **Loenamine**. 
12. Valige **Loo SAS-luba ja URL**.
13. Kopeerige ja salvestage väärtus **Bloobi SAS-i URL-i** väljale. Seda väärtust kasutatakse järgmises sammus ja sellele viidatakse kui *jagatud juurdepääsu allkirja URI-le*.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Võtmehoidla seadistamine salvestusruumi konto URI talletamiseks

1. Avage võtmehoidla, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.
2. Avage **Sätted** \> **Saladused** ja seejärel valige **Loo/impordi**, et luua uus saladus.
3. Valige lehel **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.
4. Sisestage saladuse nimi. Seda nime kasutatakse teenuse seadistamiseks teenuses Regulatory Configuration Service (RCS) ja sellele viidatakse kui *võtmehoidla saladuse nimele*.
5. Sisestage väljale **Väärtus** jagatud juurdepääsuga allkiri, URI, mille kopeerisite eelmises protseduuris ja seejärel valige käsk **Loo**.
6. Seadistage juurdepääsupoliitika, et anda elektroonilise arvelduse lisandmoodulile õigel tasemel turvaline juurdepääs loodud saladusele. Avage **Sätted \> Juurdepääsupoliitika** ja valige **Lisa juurdepääsupoliitika**.
7. Seadke saladuselubadeks toimingud **Hangi** ja **Loetle**.

    ![Teenusele juurdepääsu andmine.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Seadke serdilubadeks toimingud **Hangi** ja **Loetle**.

    ![Serdiloa andmine.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Väljal **Valige subjekt**, valige **Pole valitud**.
10. Valige subjekt dialoogiboksis **Subjekt** **elektroonilise arvelduse lisandmooduli** lisamise kaudu.
11. Valige **Lisa** ja seejärel **Salvesta**.
12. Kopeerige lehel **Ülevaade** võtmehoidla väärtus **DNS-i nimi**. Seda väärtust kasutatakse teenuse seadistamisel RCS-is ja sellele viidatakse kui *võtmehoidla URI-le*.

> [!NOTE]
> Ladustamiskonto täiendava turbe jaoks konfigureerige ladustamiskonto Azure Defender.
> 
> Lisateabe saamiseks vt [sissejuhatust ladustamiseks mõeldud Azure Defenderisse](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
