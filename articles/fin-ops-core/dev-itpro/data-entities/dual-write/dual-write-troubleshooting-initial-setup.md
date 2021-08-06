---
title: Poradce při potížích s počáteční instalací
description: Toto téma obsahuje informace, které vám mohou pomoci vyřešit problémy, které mohou nastat při počátečním nastavení integrace dvojího zápisu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 0e7316d7749566b74835acded0addb2fa4b0e858
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542408"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Poradce při potížích s počáteční instalací

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Konkrétně obsahuje informace, které vám mohou pomoci vyřešit problémy, které mohou nastat při počátečním nastavení integrace dvojího zápisu.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Nemůžete propojit aplikaci Finance and Operations s Dataverse

**Požadovaná role pro nastavení dvojitého zápisu:** Správce systému v aplikacích Finance and Operations a prostředí Dataverse.

Chyby na stránce **Nastavení odkazu na Dataverse** jsou obvykle způsobeny neúplnými problémy s nastavením nebo oprávněními. Zajistěte, aby celá kontrola stavu prošla na stránce **Nastavení odkazu na Dataverse**, jak je znázorněno na následujícím obrázku. Nemůžete propojit dvojí zapisování, pokud celý stav nepřechází na kontrolu stavu.

![Úspěšná kontrola stavu.](media/health_check.png)

Musíte mít pověření správce klienta Azure AD, chcete-li propojit prostředí Finance and Operations a Dataverse. Po propojení prostředí se uživatelé mohou přihlásit pomocí svých pověření účtu a aktualizovat existující mapu tabulek.

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Chyba při otevření odkazu na stránku Dataverse

**Požadovaná pověření pro opravu problému:** Správce klienta Azure AD

Může se zobrazit následující chybová zpráva při otevření stránky **Odkaz na Dataverse** v aplikaci Finance and Operations:

*Stavový kód odpovědi neoznačuje úspěch: 404 (Nenalezeno).*

K této chybě dojde v případě, že nedojde k dokončení kroku souhlasu. Chcete-li ověřit, zda byl krok souhlasu vyplněn, přihlaste se k portal.Azure.com pomocí účtu správce klienta Azure AD a zjistěte, zda se aplikace třetí strany s ID **33976c19-1db5-4c02-810e-c243db79efde** zobrazí v seznamu Azure AD **Podnikové aplikace**. Pokud tomu tak není, musíte zadat souhlas s aplikací.

Chcete-li poskytnout souhlas s aplikací, postupujte podle následujících kroků.

1. Otevřete následující adresu URL pomocí vašich pověření správce. Měli byste být vyzváni k zadání souhlasu.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Výběrem **Přijmout** označíte, že udělujete souhlas s instalací aplikace, která má ID **33976c19-1db5-4c02-810e-c243db79efde** ve vašem klientovi.

    > [!TIP]
    > Tato aplikace je požadována pro propojení aplikací Dataverse a Finance and Operations. Pokud máte s tímto krokem potíže, otevřete prohlížeč v anonymním režimu (v aplikaci Google Chrome) nebo v režimu InPrivate (v Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Ověřte, zda jsou při propojování správně nastaveny data společnosti a týmy s duálním zápisem

Chcete-li zajistit správnou funkci dvojího zapisování, budou v prostředí Dataverse vytvořeny společnosti, které vyberete během konfigurace. Ve výchozím nastavení jsou tyto společnosti určeny jen pro čtení a vlastnost **IsDualWriteEnable** je nastavena na **True**. Kromě toho se vytvoří výchozí vlastník organizační jednotky a tým, který obsahuje název společnosti. Před povolením map se ujistěte, zda je zadán výchozí vlastník týmu. Chcete-li najít tabulku **Společnosti (CDM\_Společnost)**, postupujte podle následujících kroků.

1. V aplikaci Customer Engagement vyberte filtr v pravém horním rohu.
2. V rozevíracím seznamu vyberte **Společnost**.
3. Výsledky zobrazíte výběrem možnosti **Spustit**.
4. Vyberte společnost, která byla propojena při konfiguraci dvojího přepisu.
5. Ověřte, zda má sloupec **Výchozí vlastnící tým** hodnotu. Na následujícím obrázku je sloupec **Výchozí vlastnící tým** nastaveno na **USMF dvojí zápis**.

    ![Ověřování výchozího vlastnícího týmu.](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Najít limit počtu právnických osob nebo společností, které lze propojit s dvojím zapisováním

Při pokusu o povolení map se může zobrazit následující chybová zpráva:

*Chyba dvojího zápisu – registrace modulu plug-in se nezdařila: \[(nelze získat mapu oddílu pro projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Chyba překračuje maximální počet povolených oddílů pro mapování DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\]. došlo k jedné nebo více chybám.*

Aktuální limit při propojení prostředí je přibližně 40 právnických osob. K této chybě dojde, pokud se pokusíte povolit mapy a mezi prostředími je propojeno více než 40 právnických osob.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]