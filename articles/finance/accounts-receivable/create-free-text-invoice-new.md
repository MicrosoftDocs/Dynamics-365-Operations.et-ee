---
title: Vabas vormis arve loomine
description: Selles teemas kirjeldatakse vabas vormis arvete loomist.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e9578d9b2d61f241ab5e92fc9740b88b80969f6
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392881"
---
# <a name="create-a-free-text-invoice"></a>Vabas vormis arve loomine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse vabas vormis arvete loomist. Selle protseduuri jaoks kasutage demoettevõtte **USMF** andmeid.

## <a name="create-a-free-text-invoice"></a>Vabas vormis arve loomine

1. Avage **Müügireskontro (või Müügiregister) \> Arved \> Kõik vabas vormis arved**.
2. Valige suvand **Uus**.
3. Valige väärtus väljal **Kliendi konto**.

    * Vaikimisi kasutatakse arvekontona sama kontot, mis on valitud kliendikontoks.
    * Kui arve pole sisestatud, algab raamatupidamisolek sõnaga **Pooleli**.
    * Pärast arve sisestamist määratakse arve number.
    * Kui kasutate ühtse euromaksete piirkonna (SEPA) lubasid, sisestatakse kliendikonto valimisel otsekorralduse luba automaatselt.

4. Sisestage väärtus väljal **Kirjeldus**.
5. Määrake dimensioonideta kontonumber väljal **Põhikonto**. Selles teemas saate hiljem sisestada ka dimensioonid.

    Samuti saate konto leidmiseks kasutada otsingut, sisestades põhikonto kohta ühe või mitu märki.

6. Põhikontole dimensioonide lisamiseks valige kiirkaart **Rea üksikasjad**.
7. Valige vahekaart **Finantsdimensiooni rida**.

    * Dimensioonid on ette nähtud ainult valitud reale.
    * Käibemaksugrupp täidetakse kliendi põhjal. Kui kliendil pole käibemaksugruppi, kasutatakse põhikonto käibemaksugruppi.
    * Kauba käibemaksugrupp täidetakse põhikontolt. Kui põhikontol pole kauba käibemaksugruppi, kasutatakse pearaamatu käibemaksuparameetrite lehel määratud kauba käibemaksugruppi.

8. Valikuline: sisestage arv väljale **Kogus**.
9. Valikuline: sisestage arv väljale **Ühiku hind**.

    Summa arvutamiseks korrutatakse kogus ühikuhinnaga. Teil on ka võimalus see arvutus tühistada, sisestades summa.

10. Arve jaoks arvutatud käibemaksu kuvamiseks valige suvand **Käibemaks**.

    Käibemaksusummasid saate vaadata sellel lehel või tühistada summad vahekaardil **Korrigeerimine**.

11. Valige **OK**.
12. Arvele tasu lisamiseks klõpsake valikut **Tasud**.
13. Sisestage väärtus väljale **Tasukood**.
14. Sisestage arv väljale **Tasude väärtus**.
15. Sulgege leht.
16. Lõpparve üksikasjade ja kogusummade kuvamiseks valige suvand **Kogusummad**.
17. Valige suvand **Sule**.
18. Arve sisestamiseks valige suvand **Sisesta**. Enne tegelikult sisestamist on teil veel võimalus tühistada.

    * Saate muuta arve printimise aega. Valige **Praegune**, et printida arve pärast värskendamist. Valige **Pärast**, et printida pärast kõikide arvete uuendamist.
    * Muutke väärtust väljas **Krediidilimiidi tüüp**, et muuta seda, kuidas kliendi krediidilimiiti enne arve sisestamist kontrollitakse.
    * Saate valida **vabas** **vormis** arve sisestamise peatamise, kui lehel Müügireskontro parameetrid (**Müügireskontro > Müügireskontro parameetritega > ilmneb tõrge).** Valige **Jah** vabas **vormis arvete sisestamise peatamiseks esimesel tõrkeparameetril**, et peatada vabas vormis arvete sisestamine tõrke ilmnemisel. Partiisse sisestamisel peatab tõrge sisestamisprotsessi ja partii olekuks seatakse **Tõrge**. Kui see suvand pole valitud, jätab sisestamisprotsess arve sisestamisveaga vahele ja jätkab lisaarvete sisestamist. Partiisse sisestamisel ei takista sisestamistõrge teiste arvete sisestamist. Partii olek **lõpetatakse**. Üksikasjalik sisestusprotsessi aruanne on pakett-tööde ajaloos läbivaatamiseks saadaval.
    * Arve printimiseks määrake suvand valikule **Jah**.
    * Arve sisestamiseks määrake suvand valikule **Jah**. Saate arve ilma sisestamata printida.

19. Valige **OK**.

## <a name="copy-lines"></a>Kopeeri read
Vabas vormis arve ridade kopeerimiseks valige üks või mitu rida ja valige suvand **Kopeeri valitud read**. Saate määrata koopiate arvu ning kopeerida märkusi ja manuseid. Saate kopeerida jaotused või lubada sisestamisel nende uuesti loomise.

Pärast ridade kopeerimist saate redigeerida teavet vajaduse järgi.

## <a name="create-a-free-text-invoice-from-a-template"></a>Vabas vormis arve loomine mallist
Saate luua vabas vormis arve mallist. Kui valite suvandi **Uus mallist** vahekaardil **Arve**, saate uue vabas vormis malli jaoks valida malli nime ja kliendikonto. Vaikeväärtusi, nt maksetingimused ja makseviisi, saab automaatselt kliendi põhjal täita või võite kasutada malli salvestatud väärtusi.

Luuakse uus vabas vormis arve, mille väärtusi saate vajaduse järgi redigeerida.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Vabas vormis arvete töövoo oleku lähtestamine väärtuselt Parandamatu väärtusele Mustand
Taastamatu tõrke tõttu peatatud töövoo eksemplaril on töövoo olekuks **Parandamatu**. Kui kliendi vabas vormis arve töövoo **olek on Taastamatu**, saate selle lähtestada olekuks Mustand **,** valides töövoo **tegevustest** tagasikutsumise. Seejärel saate redigeerida kliendi vabas vormis arvet. See funktsioon on saadaval, **kui funktsioonihalduse lehel on** vabas **vormis arvete töövoo oleku lähtestamine parandamatust mustandparameetriks** sisse lülitatud.

Saate kasutada lehte **Töövoo ajalugu**, et lähtestada töövoo olekuks **Mustand**. Selle lehe saate avada vabas vormis **arvelt** või töövoo **> Kliendi > kaudu**. Töövoo oleku lähtestamiseks olekusse **Mustand**, valige **Tagasikutsumine**. Samuti saate lähtestada töövoo oleku Olekuks **Mustand**, **·** **valides** leheküljel Vabas vormis arve või Kõik **vabas vormis arved tegevuse Tagasikutsumine.** Kui töövoo olek on lähtestatud olekusse **Mustand**, muutub see redigeerimiseks kättesaadavaks vabas **vormis arve lehel**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
