---
title: Hankija maksete kinnipidamise tingimuste loomine ja rakendamine
description: Selles teemas antakse teavet hankija maksete kinnipidamise tingimuste seadistamise ja haldamise kohta.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410213"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Hankija maksete kinnipidamise tingimuste loomine ja rakendamine

[!include [banner](../includes/banner.md)] 

Projekti jaoks hankija maksete kinnipidamise tingimuste seadistamine on kasulik, kui teie organisatsioon soovib pidada kinni osa hankijale tehtavatest maksetest. Näiteks kui soovite pidada hankijale tehtava makse kinni seni, kuni tarnitud tooted vastavad teie ootustele. Hankija maksete kinnipidamise tingimused saate täpsustada hankija lepingu tingimuste läbirääkimisel.

## <a name="create-vendor-payment-retention-terms"></a>Hankija makse kinnipidamise tingimuste loomine

Saate sisestada kinnipeetava hankija makse protsendimäära ja vabastatavate, eelnevalt kinnipeetud summade protsendimäära. Summad peetakse automaatselt hankija arvelt kinni, kuni leping jõuab määratud etappi. Pärast hankija makse kinnipidamise tingimuste seadistamist saate neid rakendada mis tahes projektide puhul, millega hankija töötab.

Hankija maksete kinnipidamise tingimuste seadistamiseks ja haldamiseks toimige järgmiselt. 

1. Avage **Projektihaldus ja raamatupidamine** > **Kinnipidamine** > **Hankija maksete kinnipidamise tingimused**.
2. Valige **Uus**, et lisada uus hankija maksete kinnipidamise tingimus. Uue tingimuse **Reegli ID** väärtus sisestatakse automaatselt. 
3. Sisestage väljale **Kirjeldus** lühike kirjeldus ja valige kiirkaardil **Tingimused** suvand **Lisa rida**, et lisada järgmised tingimuste väärtused.

   - **Tarnitud ühikute protsendimäär**: sisestage tingimuse täitmise protsent. Summad peetakse automaatselt hankija arvetest kinni, kuni projekti lõpuleviimine on jõudnud etappi, mis on võrdne kehtestatud protsendimääraga. Näiteks kui sisestate 50,00, peetakse summasid kinni seni, kuni projekt on 50 protsenti täidetud.
   - **Kinnipeetav protsendimäär**: sisestage hankija arvest kinnipeetava summa protsendimäär. Näiteks kui sisestate sellele väljale 10,00, siis peetakse hankija arvest kinni 10 protsenti summast, kuni projekt jõuab täitmisprotsendini, mille valisite väljal **Tarnitud ühikute protsendimäär**.
   - **Vabastatav protsendimäär**: valige suvand **Lisa rida**, et lisada eelnevalt kinnipeetud summade protsendimäär, mida soovite vabastada valitud projekti täitmise tasemel.

> [!NOTE]
> Kui teil on projekti erinevate tasemete täitmisel mitu vahe-eesmärki, sisestage iga kinnipidamise reegli jaoks eraldi hankija makse kinnipidamise tingimus. Igale reale saate määrata erineva kinnipeetava protsendimäära ja iga projekti taseme täitmisel vabastatava protsendimäära.

Pärast hankija jaoks hankija makse kinnipidamise tingimuste loomist saate neid tingimusi projektis rakendada.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Projektis hankija kinnipidamise tingimuste rakendamine

1. Avage **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja avage projektide loetelu lehel projekti vorm.
2. Klõpsake kiirkaardil **Hankija lepingud** valikut **Lisa rida**.
3. Tehke väljal **Konto kood** üks järgmistest valikutest. 

   - **Tabel**: hankija makse kinnipidamise tingimused kehtivad ühele hankijale.
   - **Grupp**: hankija makse kinnipidamise tingimused kehtivad kõikidele hankijagrupi hankijatele.
   - **Kõik**: hankija makse kinnipidamise tingimused kehtivad kõikidele hankijatele.

4. Valige väljal **Hankija/hankijagrupp** hankija või hankijagrupp, kellele hankija makse kinnipidamise tingimused kehtivad. Kui tegite eelmises etapis valiku **Kõik**, siis ei ole see väli saadaval.
5. Väljal **Hankija makse kinnipidamise tingimused** valige kinnipidamise tingimused, mille olete eelneva protsessi käigus loonud.
6. Kui projekti puhul on seadistatud ka hankija maksmisel tasumise tingimused, sisestage väljale **Maksmisel tasumise künnise protsendimäär** projekti künnise protsendimäär.

Hankija makse kinnipidamise tingimused kuvatakse ka hankijale loodavates ostutellimustes.
