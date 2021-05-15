---
title: Konfigureeri Azure Active Directory autentimise lubamine kassasse sisselogimiseks
description: See teema kirjeldab, kuidas konfigureerida Azure Active Directory müügis Microsoft Dynamics 365 Commerce autentimismeetodina.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937454"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigureeri Azure Active Directory autentimise lubamine kassasse sisselogimiseks

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Selles peatükis kirjeldatakse, kuidas konfigureerida Azure Active Directory (Azure AD) autentimismeetodina Microsoft Dynamics 365 Commerce kassas (POS).

Jaemüüjad, kes kasutavad koos Dynamics 365 Commerce Microsofti pilveteenustega Microsoft Azure (nt Microsoft 365) ja soovivad Microsoft Teams tavaliselt kasutada kasutaja mandaatide tsentraliseeritud haldust turvaliseks ja sujuvaks sisselogimiseks Azure AD rakendustes. Autentimise kasutamiseks Azure AD Commerce POS-i puhul peate esmalt Azure AD konfigureerima autentimismeetodina Commerce headquartersis.

## <a name="configure-pos-authentication-method"></a>POSi autentimise konfigureerimine

Commerce headquarters`is kassa autentimise meetodi redigeerimiseks tehke järgmist.
    
1. Valige suvandid **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige funktsionaalsuse profiil, mida soovite muuta.
1. **Funktsiooni** kiirkaardi jaotises **Kassa personali sisselogimine** valige soovitud autentimismeetodi suvand **sisselogimise** autentimismeetodi ripploendist.

    Sisselogimise **autentimismeetodil** on kolm valikut:
    
    - **Personali ID ja parool** – see vaikesuvand nõuab kassa kasutajatelt personali ID ja parooli sisestamist, et kassasse sisse logida ja pääseda juurde halduri alistamisfunktsioonile.
    - **Azure AD ilma ühekordse sisselogimiseta** – see valik nõuab kassa kasutajatelt mandaatide kasutamist kassasse ja juurdepääsuhalduri Azure AD alistamisfunktsioonile sisse logimiseks. Kui müügikoha klienti värskendatakse või taasavatakse, peab kassa kasutaja Azure AD sisestama mandaadid uuesti sisse logimiseks.
    - **Azure AD ühekordse sisselogimisega** – selle suvandi valimisel saavad kassa kasutajad sisse logida Pilve kassasse (CPOS), kasutades aktiivseid Azure AD mandaate, mida kasutavad teised veebirakendused samas veebibrauseris, või logida Sisse Modern POS-i (MPOS) Azure AD mandaatide abil, mis on Windowsi sisse logitud. Mõlemad meetodid võimaldavad sisselogimist ilma kassa sisselogimise ekraanile mandaate Azure AD sisestamata. Kuid kassahalduri alistamisfunktsiooni poole pöördumine nõuab siiski sisselogimist Azure AD mandaatide abil.

1. Minge jaemüügi ja äri > jaemüügi ja äri IT > jaotusgraafikusse **ja käitage** **1070 (kanali konfiguratsioon), et sünkroonida uusimad funktsiooniprofiili sätted** müügikoha klientidele.

> [!NOTE]
> - **Azure AD Autentimismeetodi ühekordse** sisselogimiseta suvand asendab Commerce'i versiooni **Azure Active Directory** 10.0.18 ja varasema variandi.
> - Azure AD autentimine nõuab aktiivset Interneti-ühendust ja see ei toimi, kui kassa on ühenduseta.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Kontode Azure AD seostamine müügikoha kasutajatega

Kassa Azure AD autentimismeetodina kasutamiseks peate kontod seostama Azure AD rakenduse Commerce headquarters kassa kasutajatega. 

Kontode Azure AD seostamiseks müügikoha kasutajatega Commerce Headquartersis järgige neid samme.
    
1. Valige **jaemüük ja äri > Töötajad > Töötajad** ja avage töötajakirje.
1. Valige tegumiriba vahekaardil **Kaubandus** grupis **Välisidentiteet**, valige **Olemasoleva identiteedi seostamine**. 
1. Dialoogiaknas **Kasuta olemasolevat välisidentiteeti** valige **Otsi kasutades e-posti**, sisestage Azure AD e-posti aadress ja seejärel valige **Otsing**.
1. Valige saadud konto Azure AD ja seejärel valige **OK**.

Pärast ülaltoodud konfiguratsioonisamme täidetakse väljad **Alias**, **UPN** ja **Väline alamidentifikaator** töötaja üksikasjade lehe vahekaardil **Kaubandus**.

Peate käitama **1060 (Personal)** töö käskudes **Retail ja Commerce > Retail ja Commerce IT > Distribution Schedule** viimase kassa kasutaja ja Azure AD konto andmete kanalisse sünkroonimiseks.

> [!NOTE]
> Hea tava on pärast töötajateabe, nt parooli, kassa loa, seotud konto või töötaja aadressiraamatu värskendamist Commerce Headquartersis käitada Azure AD **1060 (Personal) töö, et sünkroonida värskeim töötaja teave** kanalisse. Kassarakendus saab siis tuua õigeid andmeid kasutaja autentimiseks ja autoriseerimise kontrollimiseks.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Kassaluku register ja autentimine välja Azure AD logimine

Kui kassa on konfigureeritud autentimismeetodit kasutama, Azure AD ilmneb järgmine:

- **Lukustamisregistri funktsioon ei ole kassa rakenduses** saadaval. 
- Funktsioon **Lukusta** automaatselt täidetakse sama funktsiooniga **Automaatne väljalogimine**.
- Kui müügikoha kasutaja valib **väljalogimise**, palutakse kasutajal järgmisel müügikoha käivitamisel  Azure AD mandaatidega sisse logida, olenemata sellest, kas üks sisselogimine on lubatud.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Juhi alistamisfunktsioon Azure AD autentimisega

Kui müügikoht on autentimise kasutamiseks konfigureeritud, avab halduri alistamisfunktsioon dialoogiboksi, kus küsitakse halduri Azure AD kasutaja Azure AD mandaate. Kui juhatajana sisselogimine on kinnitatud, loobutakse juhataja Azure AD mandaatidest ja eelmise kasutaja Azure AD mandaate kasutatakse järgmisteks kassatoiminguteks.

> [!NOTE]
> - Commerce'i versioonides 10.0.18 ja varasemas pole halduri alistamisfunktsioon Azure AD toetatud. Personali ID-d ja parooli nõutakse ka siis, kui kassa on konfigureeritud kasutama Azure AD autentimismeetodina.
> - Kui kasutate CPOS-i Microsofti veebibrauserigaUdu iOS-seadmes, peate **blokeerimise hüpikmenüüd** Azure AD autentimisfunktsiooni funktsionaalsuse halduri sätetes välja lülitama. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Ühiskasutusega seadmete Azure AD kassapõhise autentimise turbe head tavad

Paljud jaemüüjad seadistavad oma kaupluse keskkonna viisil, et mitu kasutajat peavad kassa rakendusele juurde pääsema ühiskasutusega füüsilisest seadmest. Selles kontekstis võib see, kui üks sisselogimine pakub mugavat ja sujuvat autentimise kogemust, luua ka turbekontsessi, kus praegune kassa kasutaja ei pruugi realiseerida, et kassas kannete või toimingute tegemiseks kasutatakse teise kasutaja mandaate. Enne kassa konfigureerimist autentimismeetodi kasutamiseks on soovitatav oma turvapoliitika ja jagatud seadme sisselogimissätted üle vaadata, et otsustada, milline valik Azure AD on parim.

- Kui teie jaemüügikeskkond kasutab füüsilise seadmega sisselogimiseks ühiskasutatavaid kontosid (nt kohalikku kontot), on soovitatav kasutada valikut ilma ühekordse **Azure AD** sisselogimiseta. See tagab, et iga kassa kasutaja annab eraldi Azure AD mandaadid kassasse sisselogimiseks.
- Kui teie jaemüügikeskkond nõuab töötajatelt oma Azure AD kontode kasutamist, et kassasse sisse logida ja see majutab füüsilist seadet, on soovitatav kasutada **Azure AD ühekordse sisselogimisega** suvandit.

## <a name="additional-resources"></a>Lisaressursid

[ Töötaja konfigureerimine](tasks/worker.md)

[Jaemüügi funktsiooniprofiili loomine](retail-functionality-profile.md)


[MPOS-i ja pilve kassa laiendatud sisselogimisfunktsiooni häälestus](extended-logon.md)

[Pilve kassa turbe head tavad ühiskasutusega keskkondades](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
