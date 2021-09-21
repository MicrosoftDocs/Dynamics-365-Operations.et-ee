---
title: Kasutage hankija arvete importimiseks elektroonilist arveldamisteenust
description: See teema annab teavet selle kohta, kuidas importida hankijaarveid elektroonilise arvelduse teenuse abil.
author: gionoder
ms.date: 09/03/2021
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
ms.openlocfilehash: c28adbfe532e77a52cab7625b9539d1e8e528bea
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473372"
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
3. Sisestage **Andmekanal** vahekaardi **Parameetrid** väljagrupi **Andmekanal** väljal kanali nimi. Kanali nimi ei tohi olla suurem kui kümme tähemärki.
4. Väljale **Serveri aadress** sisestage konto pakkuja meiliaadress. Näiteks serveri aadress **https://outlook.live.com/** jaoks on **imap-mail.outlook.com**.
5. Valige **serveri port** väli ja sisestage meilikonto pakkuja kasutatav port. Näiteks serveri port **https://outlook.live.com/** jaoks on **993**.
6. Väljal **kasutajanime saladus** sisestage võtmehoidla saladus, mis sisaldab meili kasutajakonto ID-d. See saladus tuleb luua Azure'i võtme hoidlas ja seadistada oma teenuse keskkonnas. 
7. Väljal **kasutaja salasõna saladus** sisestage võtmehoidla saladus, mis sisaldab meili kasutajakonto salasõna.
8. Valikuline - Sisestage väärtused **Filtrist**, **Teema filter** ja **Kuupäevafilter**.
9. Sisestage nende meiliboksikaustade nimed, kus e-kirjad saavad olla:

    - Imporditud: **põhikaustast**
    - Salvestatud pärast edukat töötlemist: **arhiivikaust**
    - Salvestatud pärast mitte edukat töötlemist: **Veakaust** Nende kaustade loomiseks meiliboksis pole vaja. Kaustad luuakse automaatselt pärast e-arve esmast importimist ja töötlemist. 
   
10. Lisage **manusefiltri** väljagrupile faili filtreerimisteave. Töödeldakse ainult neid manuseid, mis rahuldavad määratletud filtrit. Näiteks saate seadistada "\*.xml-laiendiga manuste jaoks. Manuse nime kasutatakse seadistuses Dynamics 365 Finance või Dynamics 365 Supply Chain Management selle ajal. 
11. Vahekaardil **Kohaldatavusreeglid** vaadake kriteeriumid üle ja vajadusel värskendage neid. Väli **Kanal** peab võrdne olema varem antud **andmekanaliga**. Lisateavet vt jaotisest [Kohaldatavuse reeglid](e-invoicing-configuration-rcs.md#applicability-rules).
12. Valige **Salvesta** ja sulgege leht.

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

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Hankija arve impordi seadistamine rakendustes Finance või Supply Chain Management
Viige järgmised kaks jaotist läbi erinevate hankijaarvete impordi tüüpide häälestamiseks.

### <a name="import-brazilian-nf-e-from-email"></a>Brasiilia NF-e import meilist

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
2. Valige **kliendiarve kontekstimudel** ja seejärel valige tuletatud konfiguratsiooni loomiseks suvand **Loo konfiguratsioon** > **Tuletatud nimest: kliendiarve kontekstimudel, Microsoft**.
3. **Mustand** versioonis valige **Kujundaja** ja **Andmemudel** puus valige seejärel **andmeallikale vastendamismudel**.
4. Valige **definitsioonid** puus **Andmekanal** ja seejärel käsk **Kujundaja**.
5. **Andmeallikate** puus laiendage **$Context\_Kanal** konteiner. Valige **Väärtus** väljal suvand **Redigeeri** ja sisestage andmekanali nimi. Sisestage väljale kanal antud elektroonilise arveldamise funktsiooni andmekanali konfiguratsiooniks RCS-s. 
7. Valige **Salvesta** ja sulgege leht.
8. Sulgege leht.
9. Valige äsja loodud tuletatud konfiguratsioon ja valige **kliendiarve kontekstimudelist** ja **Versioonid** kiirkaardilt valige **Muutke olekut** > **lõpetatud**.
10. Minge **organisatsiooni halduse** > **seadistus** > **elektroonilise dokumendi parameetrid** ja **Funktsioonid** vahekaardil veenduge, et **PEPPOL Globaalne elektrooniline arveldus** on valitud. 
11. Valige **Väliskanalid** vahekaardil **Kanalid** väljagrupis suvand **Lisa**.
12. Sisestage andme kanali nimetus **Kanal** väljale ja lisage kirjeldus **Kirjeldus** väljale.
13. Väljas **Ettevõte** valige juriidiline isik. 
14. Valige **dokumendi konteksti** väljal uus tuletatud konfiguratsioon **kliendiarve kontekstimudelis**. Vastendamise kirjeldus peaks olema **andmekanali kontekst**.
15. Väljagrupis **Impordi allikad** valige käsk **Lisa**.
16. Väljale **Nimi** sisestage **Manuste filtri nimi** ja valige **andmeüksuse nime** väljal **Hankija arve päis**.
17. Valige **mudeli vastendamise** väljal **hankija arve import - importige hankija arve**.
18. Klõpsake nuppu **Salvesta** ja sulgege seejärel leht.


## <a name="receive-electronic-invoices"></a>Elektrooniliste arvete vastuvõtmine

Elektroonilise arveldamise teenus täidab kaks sammu arve importimise ajal andmekanalitest:

1. Pääseb e-kirja boksi ja loeb e-posti.
2. Töötleb e-kirjad. 
    
Nende kahe etapi sooritamiseks peab klient teenuse iga sammu jaoks käsitsi välja kutsuma. Siiski soovitame seadistada partii elektrooniliste dokumentide vastuvõtuks.

Et saada elektrooniisi arveid, järgige neid samme:

1. Avage **Organisatsiooni haldus** > **Perioodiline** > **Elektroonilised dokumendid** > **Võta vastu elektroonilised dokumendid**.
2. Valige **Ok** ja sulgege seejärel leht.


## <a name="view-receive-logs-for-electronic-invoices"></a>Elektrooniliste arvete vastuvõtulogide kuva

Elektrooniliste arvete vastuvõtulogide vaatamiseks minge **organisatsiooni administreerimise** > **perioodiline** > **Elektroonilised dokumendid** > **Elektrooniliste dokumentide vastuvõtu logi**.
Kui te ei näe edukalt töödeldud arveid, eemaldage tabelifilter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
