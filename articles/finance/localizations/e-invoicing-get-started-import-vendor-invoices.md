---
title: Kasutage hankija arvete importimiseks elektroonilist arveldamisteenust
description: See teema annab teavet selle kohta, kuidas importida hankijaarveid elektroonilise arvelduse teenuse abil.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751248"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Kasutage hankija arvete importimiseks elektroonilist arveldamisteenust

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

See teema pakub teavet, mis aitab teil alustada hankija arvete importimist elektroonilise arveldusteenuse abil. See juhib teid läbi Regulatory Configuration Services (RCS), Dynamics 365 Finance ja Dynamics 365 Supply Chain Management konfiguratsioonietappide, mida tuleb järgida hankijalt elektrooniliste arvete saamiseks.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Hankija arve impordi häälestus RCS-is
Hankija arve importimise häälestamiseks RCS-s järgige neid samme:

1. Vaadake [üldiselt saadaolevaid elektroonilise arvelduse funktsioone](e-invoicing-configuration-rcs.md#generally-available-features).
2. Valige ja importidega elektroonilise arvelduse funktsioon. Rohkem informatsiooni vaata [Microsoft konfiguratsioonipakkujalt elektroonilise arvelduse funktsiooni importimine](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Looge oma organisatsioonile elektrooniline arveldusfunktsioon. Rohkem informatsiooni vaata [Looge elektroonilise arvelduse funktsioon teie organisatsiooni teenuspakkuja all](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>E-maili konto kanali konfigureerimine

Konfigureerige e-posti konto kanal, kui teie loodud elektroonilise arveldamise funktsioon impordib lisatud failidest elektroonilise hankija arveid, mis on vastu võetud meiliga.

1. RCS-is valige loodud elektroonilise arvelduse funktsioon. Veenduge, et valite versiooni olekuga **Mustand**.
2. Vahekaardil **Häälestus** ruudustikus valige päringu seadistus ja seejärel valige **Redigeeri**.
3. vahekaardil **Andmekanal** väljal **Parameetrid** valige **Serveri aadress** ja sisestage e-posti konto pakkuja.
4. Valige **serveri port** ja sisestage meilikonto pakkuja kasutatav port.
5. Valige **kasutajanime saladus** ja sisestage võtmehoidla saladus, mis sisaldab meili kasutajakonto ID-d.
6. Valige **kasutajanime saladus** ja sisestage võtmehoidla saladus, mis sisaldab meili kasutajakonto parooli.
7. Valige **teemafilter**. Vaadake üle ja värskendage stringi, mis sisaldab vaikemeili, et tuvastada meil, mis sisaldab importimiseks elektroonilist hankija arvet.
8. Vahekaardil **Kohaldatavusreeglid** vaadake kriteeriumid üle ja vajadusel värskendage neid. Lisateavet vt jaotisest [Kohaldatavuse reeglid](e-invoicing-configuration-rcs.md#applicability-rules).
9. Valige **Salvesta** ja sulgege leht.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Microsoft SharePoint kanali konfigureerimine

Konfigureerige Microsoft SharePoint kanal, kui elektroonilise arveldamise funktsioon impordib elektroonilisi hankija arveid kaustadesse paigutatud SharePoint failidest.

1. RCS-is valige loodud elektroonilise arvelduse funktsioon. Veenduge, et valite **versiooni** olekuga **Mustand**.
2. Vahekaardil **Häälestus** ruudustikus valige funktsiooni seadistus ja seejärel valige **Redigeeri**.
3. Vahekaardil **Andmekanal** väljal **Parameetrid** valige **SharePoint aadress** ja sisestage SharePoint URL.
4. Valige **serveri port** ja sisestage meilikonto pakkuja kasutatav port.
5. Valige **Rakenduse ID** ja sisestage võtmehoidla saladus, mis sisaldab SharePoint kliendi ID-d.
6. Valige **Rakenduse saladus** ja sisestage võtmehoidla saladuse nimi, mis sisaldab SharePoint kliendi salasõna.
7. Valige **Faili filter**. Vaadake üle ja värskendage maski impordiks elektroonilist hankijaarvet sisaldavate failide filtreerimiseks.
8. Vahekaardil **Kohaldatavusreeglid** vaadake kriteeriumid üle ja vajadusel värskendage neid. Lisateavet vt jaotisest [Kohaldatavuse reeglid](e-invoicing-configuration-rcs.md#applicability-rules).
9. Valige **Salvesta** ja sulgege leht

### <a name="deploy-an-electronic-invoicing-feature"></a>Elektroonilise arvelduse funktsiooni juurutamine

Elektroonilise arveldamise funktsiooni juurutamiseks vaata [Juurutage elektroonilise arvelduse lisandmoodul teenuse keskkonda](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Hankija arve impordi seadistamine rakendustes Finance ja Supply Chain Management
Viige järgmised kaks jaotist läbi erinevate hankijaarvete impordi tüüpide häälestamiseks.

### <a name="import-vendor-invoices-from-email"></a>Hankija arvete importimine meilist

1. Logige oma Finance või Supply Chain Management keskkonda sisse ja veenduge, et oleksite õiges juriidilises isikus.
2. Avage **Organisatsiooni halduses** > **Seadistus** > **Elektroonilise dokumendi parameetrid**.
3. Vahekaardil **Funktsioonid** veenduge, et **NF-e Föderaalne - Brasiilia elektrooniline arve** on valitud.
4. Valige **Väliskanalid** vahekaardil **Kanalid** väljagrupis suvand **Lisa**.
5. Sisestage väljale **Kanal** sisestage **NFe** (kanali nimi, mis on antud RCS-i elektroonilise arveldamise funktsiooni andmekanali konfiguratsioonis).
6. Väljale **Kirjeldus** sisestage kirjeldus. Väljas **Ettevõte** valige juriidiline isik.
7. Valige väljal **Dokumendi kontekst** suvand **Fiskaal dokumendi sisu – kliendi arve konteksti mudel**.
8. Väljagrupis **Impordi allikad** valige käsk **Lisa**.
9. Väljale **Nimi** sisestage **XmlFile** (nimi, mis on **Manuse filter** on elektroonilise arveldamise funktsiooni andmekanali konfiguratsioonis RCS-is).
10. Sisestage **Kirjeldus** väljale kirjeldus ja valige andmeüksuse nime väljal **Andmete olemi nimi** valige **Vastuvõetud NF-e XML-dokumendid**.
11. Väljal **mudeli vastendamine** valige **NF-e posti import – NF-e e-posti import (BR)** ja seejärel valige **Salvestamine**.
12. Valige **elektroonilise dokumendi** vahekaardi jaotises **Elektrooniline aruandlus** suvand valige **Lisa** ja **Tabeli nimi** väljal valige **Vastu võetud NF-e XML-dokument**.
13. Valige väljal **Dokumendi kontekst** suvand **Uuri dokumendi sisu – kliendi arve kontekst**.
14. Väljal **Elektroonilise dokumendi mudeli vastendamine** valige suvand **Uuri vastendamist – fiskaal dokumendi vastendamine**.
15. Valige **Vastuse tüübid** ja seejärel **Uus**.
16. Väljal **Vastuse tüüp** sisestage **Vastus**. Valige väljal **Edastuse olek** suvand **Ajastatud**.
17. Valige väljal **Mudelivastendus** suvand **Mudeli vastendamine vastusteatest – vastussõnumi impordi vorming**.
18. Valige **Salvesta** ja sulgege seejärel leht.

### <a name="import-peppol-electronic-vendor-invoices"></a>PEPPOL elektroonilise hankija arvete importimine

1. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
2. Valige **kliendiarve kontekstimudel** ja looge tuletatud konfiguratsioon.
3. Valige **mustand** versioonis suvand **Kujundaja**.
4. Valige **andmemudeli** puus **kliendiarve** ja seejärel valige **andmeallikale vastendamismudel**.
5. Valige **definitsiooni** puus **KliendiArve** ja seejärel käsk **Kujundaja**.
6. Puus **Andmeallikad** valige suvand **Väli\_Kanal**. Valige **väärtus** väljal **PEPPOL**. Sisestage väljale kanal antud elektroonilise arveldamise funktsiooni andmekanali konfiguratsiooniks RCS-s. 
7. Valige **Salvesta** ja sulgege leht.
8. Sulgege leht.
9. Valige **kliendiarve kontekstimudel** ja valige **Versioonid** kiirkaardil suvand **Muuda olekut** > **lõpetatud**.
10. Minge **organisatsiooni halduse** > **seadistus** > **elektroonilise dokumendi parameetrid** ja **Funktsioonid** vahekaardil veenduge, et **PEPPOL Globaalne elektrooniline arveldus** on valitud. 
11. Valige **Väliskanalid** vahekaardil **Kanalid** väljagrupis suvand **Lisa**.
12. Sisestage **Kanal** väljale **PEPPOL**. Väljale **Kirjeldus** sisestage kirjeldus.
13. Väljas **Ettevõte** valige juriidiline isik. Valige väljal **Dokumendi kontekst** suvand **Kliendi arve sisu – kliendi arve konteksti mudel**.
14. Valige **Salvesta** ja sulgege seejärel leht.


## <a name="receive-electronic-invoices"></a>Elektrooniliste arvete vastuvõtmine
Et saada elektrooniisi arveid, järgige neid samme:

1. Avage **Organisatsiooni haldus** > **Perioodiline** > **Elektroonilised dokumendid** > **Võta vastu elektroonilised dokumendid**.
2. Valige **Ok** ja sulgege seejärel leht.

## <a name="view-receive-logs-for-electronic-invoices"></a>Elektrooniliste arvete vastuvõtulogide kuva

Elektrooniliste arvete vastuvõtulogide vaatamiseks minge **organisatsiooni administreerimise** > **perioodiline** > **Elektroonilised dokumendid** > **Elektrooniliste dokumentide vastuvõtu logi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
