---
title: Äripartnerist kasutajate haldamine B2B e-kaubanduse veebisaitidel
description: See teema kirjeldab, kuidas lisada, kustutada ja redigeerida Microsoft Dynamics 365 Commerce äripartneri kasutajaid ettevõtete vahel (B2B) e-kaubanduse veebisaitidel ja Commerce Headquartersis.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ef8ae583f18048fc6a36adf38ee7be0fb5b02fcd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686320"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Äripartnerist kasutajate haldamine B2B e-kaubanduse veebisaitidel

[!include [banner](../../includes/banner.md)]

See teema kirjeldab, kuidas lisada, kustutada ja redigeerida Microsoft Dynamics 365 Commerce äripartneri kasutajaid ettevõtete vahel (B2B) e-kaubanduse veebisaitidel ja Commerce Headquartersis.

> [!NOTE]
> - Dokumendi [eeltingimuseks on B2B-äripartnerite](partners-customer-hierarchies.md) haldamine, kasutades kliendi hierarhiate teemat.
> - Veenduge, et lähtestate dokumenditüüpide üksuse Commerce Headquartersis, avades **dokumenditüüpide** vormi Organisatsioonihalduse **dokumendihalduse \> dokumenditüüpides \>**.

B2B e-kaubanduse veebisaidid nõuavad, et organisatsioonide äripartneriks saamiseks registreeruksid. Pärast seda, kui organisatsioon esitab registreerimisandmed B2B e-äri veebisaidile, läbib registreerimistaotlus kvalifikatsiooniprotsessi. Kui organisatsioon on edukalt kvalifitseeritud, võetakse see äripartnerina vastu.

Kui organisatsioon on äripartneriks võetud, määratakse administraatoriks organisatsiooni see kasutaja, kes algatas äripartneriks saamise, ja talle antakse õigus liita B2B e-kaubanduse veebisaidile täiendavaid volitatud kasutajaid. Need volitatud kasutajad saavad seejärel esitada tellimusi äripartneri nimel.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Administraatorkasutajate seadistamine uue äripartneri jaoks

Potentsiaalsed äripartnerid saavad käivitada sisseseadmisprotsessi B2B e-äri veebisaidile, esitades sisseostmistaotluse B2B veebisaidi lingi kaudu. Siis saavad nad kasutada kohandatavat vormi, et pakkuda üksikasju, mis on vajalikud sisse- ja välja registreerimiseks. Pärast taotluse esitamist kuvatakse esitamise kinnituse leht. Kui esitamine kinnitatakse, muutub ettevõte, mille jaoks taotlus esitati, äripartneriks ning nõudeja (kes algatas sisseseadmistaotluse) äripartneri administraatoriks.

Äripartneri taotluse kinnitamiseks Commerce Headquartersis järgige neid samme.

1. Avage **Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käivitage töö **P-0001**, et tõmmata kõik äripartnerite liitumistaotlused Commerce'i peakontorisse.
1. Kui töö **P-0001 on** edukalt käitatud, **minge jaemüügi ja äri ite \>** kliendi ja käivitage klientide **ja kanali taotluste sünkroonimise** töö. Pärast selle töö edukat käivitamist luuakse **Commerce Headquartersis B2B-potentsiaalse** kliendi tüübi potentsiaalsete klientidena katmistaotlused. 
1. Minge kliendi **kõigi \> potentsiaalsete klientide** juurde ja valige uue äripartneri potentsiaalse kliendi kirje potentsiaalse kliendi üksikasjade lehe avamiseks.
1. Märkige vahekaardil **Üldine** ruut Teisenda **kinnitamine \> /Tagasilükkamine**, et kinnitada sisseostmistaotlus. Kui kuvatakse kinnitusteade, kinnitage, et soovite protsessiga jätkata, ja seejärel kinnitage taotlus. Kinnitamine muudab potentsiaalse **kliendi** kirje olekuvälja väärtusele **Kinnitatud**. Seejärel saadetakse taotleja meiliaadressile meil kinnitamaks, et tema organisatsioon on äripartnerina kinnitatud. Luuakse ka kliendihierarhia, kus nõudeja lisatakse äripartneri administraatorina.

    > [!NOTE]
    > Praegu saadetakse kinnituse meil kinnitamisel kohe. Kuid tulevane Commerce'i funktsioon võimaldab administraatoril e-kirjad käsitsi käivitada.

1. Minge jaemüügi **ja äri it-jaotuse \>** **graafikusse ja käivitage 1010 (kliendid)** töö, et suunata uued kliendi ja kliendi hierarhia kirjed kanali andmebaasi.

> [!NOTE]
> Tagamaks, et uued kliendikirjed saadetakse kanali andmebaasi, peab vähemalt üks kliendiga seotud aadressiraamatutest olema kaasatud võrgupoega seostatud kliendi aadressiraamatusse. Saate selle protsessi automatiseerida, konfigureerides e-poe vaikekliendi aadressiraamatu nii, et süsteem kopeerib aadressiraamatu väärtuse igale uuele kliendile.

Kui kliendi hierarhia kirjed on kanali andmebaasiga sünkroonitud, saab nõudeja sisse logida B2B e-äri veebisaidile, kasutades meiliaadressi, mille nad sisestasid, kui nad esitasid sisseseadmistaotluse. Kasutajad saavad kasutada registreerumisvoogu oma kontole parooli määratlemiseks. Lisateavet selle kohta Azure Active Directory, kuidas lubada (Azure AD) B2C-identiteedi pakkuja kirje linkimine potentsiaalse kliendi kinnitusel loodud B2B kliendikirjega, vt [Luba automaatne linkimine](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Teatage B2B-potentsiaalseid kliente, kui need on kinnitatud või tagasi lükatud

Kui kinnitate või lükkate tagasi B2B potentsiaalse kliendi taotluse, saab meiliteatise potentsiaalsele kliendile automaatselt saata.

Commerce Headquartersis **kinnitatud B2B-potentsiaalse kliendi või B2B-potentsiaalse** **kliendi** tagasilükatud teatise tüübi sündmuste kohta meiliteatiste häälestamiseks järgige neid samme.

1. Looge meilimallid e-kirjade jaoks **, mis saadetakse potentsiaalsetele klientidele, kui B2B-potentsiaalne** **klient on kinnitatud või B2B** potentsiaalse kliendi tagasilükatud teavitustüüp käivitatakse. Lisateavet nende teatisetüüpide toega seotud kohatäitjate kohta vt teatise [tüüpidest](../email-templates-transactions.md#notification-types). Teabe saamiseks e-kirja mallide loomise kohta vt teemast [E-kirja malli loomine](../email-templates-transactions.md#create-an-email-template).
1. **Lisage B2B-potentsiaalne klient** **kinnitatud ja B2B-potentsiaalse** kliendi tagasilükatud teatisetüübid oma meiliteatise profiili ja vastendage need loodud meilimallidega. Lisateavet meiliteatise profiilide häälestamise kohta vaata [häälestage meiliteatise profiil](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Täiendavate äripartneri kasutajate liitmine

Äripartneri administraatorkasutaja saab vajadusel B2B e-kaubanduse veebisaidile lisada täiendavaid äripartneri kasutajaid.

B2B e-kaubanduse veebisaidile äripartnerite lisamiseks toimige järgmiselt.

1. Logige B2B e-kaubanduse veebisaidile administraatorina sisse.
1. Avage **Minu konto \> Organisatsiooni kasutajad \> Vaata üksikasju** ja valige **Lisa kasutaja**.
1. Sisestage nõutud teave ja seejärel valige **Salvesta**. Uue kasutaja olekuks seadistatakse **Ootel**.

Kui P-0001 **·** **ja** Sünkrooni kliendid ja kanali taotlused on käitatud, **luuakse** Commerce Headquartersis uue kasutaja jaoks klienditüüp Isik. See kliendikirje on seotud ka vastava äripartnerist kliendi hierarhia kirjega. Lisaks saadetakse e-kiri uue kasutaja meiliaadressile, et teavitada teda äripartneri organisatsiooni kasutajaks lisamisest ja sellest, et ta saab nüüd B2B e-kaubanduse veebisaidile sisse logida.

Järgmisena käivitage **1010 -töö (Kliendid),** et sünkroonida uus äripartneri kasutaja kanali andmebaasiga.

Kui kliendikirje on sünkroonitud, on B2B e-äri **veebisaidi kasutaja olekuks seadistatud Aktiivne** ja uus kasutaja saab oma meiliaadressi kasutades B2B e-commerce'i veebisaidile sisse logida. Kasutajad saavad kasutada registreerumisvoogu oma kontole parooli määratlemiseks. Lisateavet, kuidas Azure AD lubada B2C-identiteedi pakkuja kirje linkimine Commerce Headquartersis loodud B2B kliendikirjega, vt Luba [automaatne linkimine](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Äripartneri kasutaja üksikasjade redigeerimine

Äripartneri kasutajate üksikasjade redigeerimiseks järgige neid samme.

1. Logige B2B e-kaubanduse veebisaidile administraatorina sisse.
1. Avage **Minu konto \> Organisatsiooni kasutajad \> Kuva üksikasjad** valige nupp **Redigeeri** (pliiatsi sümbol), tehke vajalikud muudatused ja seejärel valige nupp **Salvesta**. Muudatused jõustuvad alles pärast seda **, kui P-0001**, **·** **klientide ja kanali taotluste sünkroonimine ja 1010 (kliendid)** tööd on käitatud.

## <a name="remove-a-business-partner-user"></a>Äripartneri kasutaja eemaldamine

Administraator saab vajadusel eemaldada äripartneri organisatsiooni olemasoleva kasutajad nende kasutajate loendist, kellel on juurdepääs B2B e-kaubanduse veebisaidile.
Äripartneri kasutaja eemaldamiseks toimige järgmiselt.
- Logige B2B e-kaubanduse veebisaidile administraatorina sisse.
- Minge vormile **Minu konto > Organisatsiooni kasutajad \> vaadake** üksikasju ja valige nupp **Eemalda** (sümbol X). Kui kuvatakse kinnitusteade, kinnitage, et soovite kasutaja eemaldada. Muudatus jõustub ainult pärast seda **, kui P-0001**, **·** **klientide ja kanali taotluste sünkroonimine ja 1010 (kliendid)** tööd on käitatud.

> [!NOTE]
> Kui eemaldate kasutaja B2B e-kaubanduse veebisaidile juurdepääsu omavate kasutajate hulgast, eemaldatakse vastav kasutajakirje äripartneri kliendi hierarhia kirjest. Kuid kliendikirjet ennast Commerce'i peakontorist ei kustutata.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Olemasolevad kliendid B2B e-äri veebisaidi äripartneritena

Administraatorid saavad äripartnereid ja kasutajaid otse Commerce'i peakontorist vastu võtta. See võimalus on kasulik oma olemasolevate äripartneritele B2B e-kaubanduse veebisaidi kaudu.

Äripartnerite ja kasutajate vastuvõtmiseks Commerce'i peakontorist toimige järgmiselt.

1. Looge või valige klient organisatsiooni **tüübist**, et lisada see äripartnerina.
1. Looge või valige klient tüübiga **Isik**, et see äripartnerile administraatori või kasutajana lisada. Veenduge, et esmased meiliaadressid on klientidega seostatud. Neid meiliaadressisid kasutatakse veebisaidile sisselogimiseks. 

    > [!NOTE]
    > Süsteem peab olema võimeline otsima ainulaadset kliendikirjet kasutajatele, kes saavad veebisaidile sisse logida. Kui süsteem leiab rohkem kui ühe kliendi, kellele on juriidilises isikus sama esmane meiliaadress, ei saa kasutaja veebisaidile sisse logida.

1. Looge kliendi hierarhia ID.
1. Väljale **Nimi** sisestage nimi.
1. Sisestage väljale **Organisatsioon** äripartnerist organisatsiooni klient.
1. **Valige hierarhia kiirkaardil** käsk **Lisa**.
1. **Valige väljal** Nimi klienditüüp **Isik**.
1. **Valige administraatori** roll kliendile, mis tuleks määrata administraatoriks.
1. Korrake seda protsessi klientide lisamiseks hierarhiasse.

## <a name="additional-information"></a>Lisateave

- Kõiki selles teemas mainitud töid saab konfigureerida graafikus käivituma partiivormingus. Eeldatakse, et äripartnerid konfigureerivad pakett-töid vastavalt vajadusele.
- Praegu saab adiminstraatorkasutajaks määrata ainult ühe kasutaja/kliendi kirje ja seda rolli saab muuta ainult Commerce'i peakontoris. Puudub tugi iseteeninduse võimalustele, mis laseksid äripartneritel määrata mitut administraatorit või muuta B2B e-kaubanduse veebisaitidel adiminstraatoreid.
- Kuigi kasutajatele saab määrata kulutamise piiranguid, ei ole kulutamise piirangute jõustamist tellimuse sisestamise protsessis veel rakendatud.
- Kogu kasutajakogemuse äriloogika ja valideerimine B2B e-kaubanduse veebisaidil põhineb kasutajale Commerce'i peakontoris vastendatud kliendikirje konfiguratsioonil.

## <a name="additional-resources"></a>Lisaressursid

[B2B e-kaubandussaidi häälestamine](set-up-b2b-site.md)

[B2B äripartnerite haldamine kliendihierarhiaid kasutades](partners-customer-hierarchies.md)

[Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks](payment-method.md)

[Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks](quantity-limits.md)

[Numbriseeriate ülevaade](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
