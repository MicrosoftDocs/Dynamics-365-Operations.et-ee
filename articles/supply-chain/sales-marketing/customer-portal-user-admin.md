---
title: Kliendiportaali kasutajate loomine ja haldamine (sisaldab videot)
description: See artikkel selgitab, kuidas luua kliendiportaali kasutajakontosid ja seada neile õigusi.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2d095b0f6ff707852b4c9e22fd9c31cf87ccbe9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905772"
---
# <a name="create-and-manage-customer-portal-users"></a>Kliendiportaali kasutajate loomine ja haldamine

[!include [banner](../includes/banner.md)]


Valmiskujul rakenduse puhul ei saa kasutajad ise kliendiportaali abil loodud veebisaitidesse registreerida. Sisselogimiseks ja veebisaidi kasutamiseks peab administraator kasutajatele kutse saatma. Microsoft on teadlikult blokeerinud kasutajate iseregistreerimise võimaluse.

Enne, kui kasutaja saab veebisaiti kasutada, tuleb luua sellele kasutajale kontakti kirje. See kirje näitab, millisele kliendikontole ja juriidilisele isikule kasutaja kuulub. See teave on oluline tagamaks, et kasutaja saab luua ja kuvada müügitellimusi.

Kasutajate iseregistreerumise korral luuakse neile automaatselt kontakti kirjed. Seega ei saa te tagada, et kasutaja valib õige kliendikonto ja juriidilise isiku. Kutseprotsess võimaldab aga administraatoril määrata kontakti kirjele õige kliendikonto ja juriidiline isik enne kutse saatmist. Kui mõtlete lahenduse kohandamisele, et kasutajad saaksid ise registreeruda, siis tasub kindlasti eelnevalt kaaluda võimalikke tagajärgi.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

[Kutsuda kliente oma kliendiportaali](https://youtu.be/drGUYHX9QIQ) videot registreerima ja kasutama (vt ülal kuvatud) [on kaasatud operatsioonide ja finantside](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) portaali YouTube.

## <a name="prerequisite-setup"></a>Eeltingimuste seadistamine

Power Appsi portaalides salvestatakse kontaktid Microsoft Dataverse’is tabelina üksuses **Kontaktid**. Seejärel sünkroonib topeltkirjutus need kirjed vajaduse järgi teenuses Microsoft Dynamics 365 Supply Chain Management.

![Süsteemi diagramm Customer portaali kontaktide jaoks.](media/customer-portal-contacts.png "Süsteemi diagramm kliendiportaali kontaktide jaoks")

Enne uute klientide kutsumist veenduge, et oleksite lubanud topeltkirjutuses tabeli **Kontakt** vastendamise.

## <a name="the-invitation-process"></a>Kutseprotsess

Olemasoleva kontakti kliendiportaali kutsumiseks järgige Power Appsi portaalide dokumentatsioonis toodud teemat [Oma portaalidesse kontaktide kutsumine](/powerapps/maker/portals/configure/invite-contacts).

Enne kliendi kliendiportaaliga liituma kutsumist veenduge, et kliendi [kontakti kirje](/powerapps/maker/portals/configure/configure-contacts) oleks saadaval ja seadistatud järgmisel moel.

1. Seadke välja **Ettevõte** väärtuseks juriidiline isik, kellele klient peab rakenduses Supply Chain Management kuuluma.
2. Seadke välja **Kontonumber** väärtuseks kliendi kontonumber, mis teie arvates peab kliendil rakenduses Supply Chain Management olema.

Pärast kontakti loomist peaksite nägema seda rakenduses Supply Chain Management.

Lisateavet leiate teemast [Kontakti konfigureerimine portaalis kasutamiseks](/powerapps/maker/portals/configure/configure-contacts) Power Appsi portaalide dokumentatsioonis.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Valmiskujul veebirollid ja tabeli load

Power Appsi portaalides määratletakse kasutajarollid [veebirollide](/powerapps/maker/portals/configure/create-web-roles) ja [tabeli lubade](/powerapps/maker/portals/configure/assign-entity-permissions) alusel. Mõned kliendiportaali rollid on määratletud valmiskujul. Te saate luua uusi rolle ja muuta või eemaldada olemasolevaid rolle.

### <a name="out-of-box-web-roles"></a>Valmiskujul veebirollid

Selles jaotises kirjeldatakse kliendiportaaliga kaasatulevaid veebirolle.

Lisateavet valmiskujul kasutajarollide muutmise kohta vt teemadest [Portaalidele veebirollide loomine](/powerapps/maker/portals/configure/create-web-roles) ja [Portaalidele kirjepõhise turbe lisamine tabeli lubade abil](/powerapps/maker/portals/configure/assign-entity-permissions) Power Appsi portaalide dokumentatsioonis.

#### <a name="administrator"></a>Administraator

Administraator korraldab veebisaidi järelevalvet ja haldab seda. See isik loob ja seadistab kliendiportaali. Administraator haldab portaali IT ja turbega seotud aspekte ning veendub, et kõik toimib sujuvalt. Samuti võib administraator portaali kohandada ja/või muuta, lisades uusi funktsioone, luues uusi rolle ja tehes muud.

#### <a name="customer-representative"></a>Kliendi esindaja

Kliendi esindaja töötab kliendi ettevõtte jaoks ja vastutab ettevõtte tellimuste haldamise eest. Kliendi esindaja näeb kõiki ettevõtte nimel esitatud tellimusi ja neid esitanud kasutajaid. Lisaks näeb kliendi esindaja teavet üleüldise konto ning selle kohta, millised kontaktid saavad selle konto nimel tellimusi esitada.

#### <a name="authorized-users"></a>Autoriseeritud kasutajad

Volitatud kasutajad saavad esitada tellimusi ja vaadata enda esitatud tellimuste olekut. Samas ei näe nad teiste enda ettevõtte kasutajate esitatud tellimuste olekut.

#### <a name="unauthorized-users"></a>Volitamata kasutajad

Volitamata kasutajad ei saa andmeid vaadata. Nad näevad ainult avalikku teavet, nagu näiteks tingimused ja kliendiportaali juhtiva ettevõtte üksikasjad.

#### <a name="example"></a>Näide

Järgmises tabelis on näidatud, milliseid müügitellimusi iga veebirolli kasutaja süsteemis näeb.

| Müügitellimus | Administraator | Kliendi &nbsp;X esindaja | Volitatud kasutaja: Jane | Volitatud kasutaja: Sam | Volitamata kasutaja: May |
|---|---|---|---|---|---|
| Klient&nbsp;X Tellija:&nbsp;Jane | Jah | Jah | Jah | Ei | Ei |
| Klient&nbsp;X Tellija:&nbsp;Sam | Jah | Jah | Ei | Jah | Ei |
| Klient&nbsp;Y Tellija:&nbsp;May | Jah | Ei | Ei | Ei | Ei |

> [!NOTE]
> Kuigi nii Sam kui ka Jane on kliendi X jaoks töötavad kontaktid, näevad nad ainult iseenda esitatud tellimusi ja ei midagi muud. Kuigi Mayl on süsteemis tellimus, siis ei näe ta seda tellimust kliendiportaalis, kuna ta on volitamata kasutaja. (Lisaks peab ta olema esitanud tellimuse mõne muu kanali, mitte kliendiportaali kaudu.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]